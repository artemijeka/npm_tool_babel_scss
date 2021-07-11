"info": "15.06.22 - expiring support ie 11"

# npm js babel + scss + autoprefixer + minimize developing
# v 2.0 - 12.07.2021

***https://github.com/nodesource/distributions/blob/master/README.md***
### (linux ubuntu apt):  
***https://nodejs.org/en/download/package-manager/***
```
cd /path/to/site.ru  
sudo apt install curl
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt install -y nodejs
sudo apt install -y npm
sudo apt autoremove
npm i
npm install --save-dev @babel/core @babel/cli @babel/preset-env
```
---

### (windows): 
***install nodejs with npm:***  
***https://nodejs.org/en/download/***  
***PowerShell command:***
`npm i`
---

### If `npm i` is not installed, then:
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

### Development SCSS:  
`npm run scss-dev` **or** `npm run scss-dev-alt` **could** `npm run scss-dev-u` **(if unix machine)**  
**- this will start compiling and tracking the file:**   
`/scss/styles.scss` **(and behind all connected)**,  
**then compilation, auto-prefixes and merging into one file:**  
`/css/styles.prefix.css`  

### Development JS Babel:  
  `npm run babel-dev`  
  **- this will start compiling and tracking the directory:**  
    `/js/` **(and behind all the files in it `*.js`)**  
  *(here you need to pay attention to the prefix of all `.js` file system (`50.script.js`), the order of compilation of files depends on it),*   
  **then compilation, auto-prefixes and merging into one file:**  
    `/js/scripts.js` 

### Development SCSS + JS Babel
  `npm run dev` **or** `npm run dev-alt`
---

### Build and minify SCSS:  
`npm run scss-build`  
**- does the same as:** `npm run scss-dev*`,  
**only does not monitor the file and does the minification of the file:**  
`/css/styles.prefix.min.css`  
---

### Build and minify JS Babel:           
  `npm run babel-build`        
  **- does the same as** `npm run babel-dev`
  **just doesn't follow the directory and minify the code to a file:**  
    `/js/scripts.min.js`  
---

### Build and minify SCSS + JS Babel:  
  `npm run build` **or** `npm run build-alt` **or** `npm run build-u`    