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

### Если `npm i` не устанавливается, то:
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

### Разработка SCSS:  
`npm run scss-dev` **или** `npm run scss-dev-alt` **можно** `npm run scss-dev-u` **(если unix машина)**  
**- это запустит компиляцию и слежение за файлом:**   
`/scss/styles.scss` **(и за всеми в нем подключенными)**,  
**затем компиляция, автопрефиксы и объединение в один файл:**  
`/css/styles.prefix.css`  

### Разработка JS Babel:  
  `npm run babel-dev`  
  **- это запустит компиляцию и слежение за дирректорией:**  
    `/js/` **(и за всеми в ней файлами `*.js`)**  
  *(тут надо обратить внимание на префикс всех `.js` файлов (`50.script.js`), от него зависит порядок компиляции файлов),*   
  **затем компиляция, автопрефиксы и объединение в один файл:**  
    `/js/scripts.js` 

### Разработка SCSS + JS Babel
  `npm run dev` **или** `npm run dev-alt`
---

### Сборка и минификация SCSS:  
`npm run scss-build`  
**- делает тоже самое, что и:** `npm run scss-dev*`,  
**только не следит за файлом и делает минификацию файла:**  
`/css/styles.prefix.min.css`  
---

### Сборка и минификация JS Babel:           
  `npm run babel-build`        
  **- делает тоже самое, что и** `npm run babel-dev`
  **только не следит за дирректорией и делает минификацию кода в файл:**  
    `/js/scripts.min.js`  
---

### Сборка и минификация SCSS + JS Babel:  
  `npm run build` **или** `npm run build-alt` **или** `npm run build-u`    