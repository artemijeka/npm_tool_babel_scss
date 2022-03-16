#### npm js babel + scss + autoprefixer + minimize developing   
Source: https://github.com/artemijeka/npm-tool-babel-scss   
Version: v2.1 - 16.03.2022   
Info: 15.06.22 - expiring support ie 11

---

*https://github.com/nodesource/distributions/blob/master/README.md*
#### (linux ubuntu apt):  
*https://nodejs.org/en/download/package-manager/*
```
cd /path/to/site.ru   
sudo apt install curl 
# Using Ubuntu 
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs 
sudo apt-get install -y npm 
sudo apt autoremove 
npm i 
```
---

#### (windows):   
install nodejs with npm:  
*https://nodejs.org/en/download/*  
PowerShell command:
`npm i`  

---

#### If `npm i` is not installed, then:
```
  # Update nodejs to latest version:
  sudo npm install -g n
  sudo n latest
  # Update npm to latest version:
  sudo npm install -g npm
  # Try npm install
  npm i
```
---

#### Development SCSS + JS Babel
`npm run dev`

#### Development SCSS:  
`npm run scss-dev` 
this will start compiling and tracking the file:   
`./scss/header-studios-and-imap.scss` (and behind all connected),  
then compilation, auto-prefixes and merging into one file:  
`./css/dev/header-studios-and-imap.min.css`  and
`./css/dev/header-studios-and-imap.prefix.min.css`

#### Development JS Babel:  
`npm run babel-dev`  
this will start compiling and tracking the directory:  
`./js/dev/header-studios-and-imap/` (and behind all the files in it `*.js`)  
*(here you need to pay attention to the prefix of all `.js` file system (`50.some-script.js`), the order of compilation of files depends on it),*   
then compilation, 'babeling' and merging into one file:  
`./js/header-studios-and-imap.js` and
`./js/header-studios-and-imap.min.js`

---

#### Build and minify SCSS + JS Babel:  
`npm run build`   

#### Build and minify SCSS:  
`npm run scss-build`  
- does the same as: `npm run scss-dev*`,  
only does not monitor the file and does the minification of the file:  
`/css/styles.prefix.min.css`  



#### Build and minify JS Babel:           
  `npm run babel-build`        
  - does the same as `npm run babel-dev`
  just doesn't follow the directory and minify the code to a file:  
    `/js/scripts.min.js`  

