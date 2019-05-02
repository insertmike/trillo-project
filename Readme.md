# Trillo Project - Front End
`Live:` https://insertmike.github.io/trillo-project/    

A Flexbox based design for a hotel booking site.
## Features
- Fully responsive [ *Desktop First Approach* ]
- Written completely in *HTML & CSS*    
- Used the <a href="https://sass-guidelin.es/#the-7-1-pattern" target="_blank">*7-1 SASS pattern*</a>  &  <a href="https://en.bem.info/methodology/" target="_blank">*BEM*</a>   to create scalable and maintainable code.    
 
 Designed by Jonas Schmedtmann, implemented by me.
 
 ## Project Overview
 - ### Responsiveness
    The website is fully responsive thanks to `flexbox`
 
![responsive](https://user-images.githubusercontent.com/45242072/57090929-e969dc00-6cff-11e9-8e13-a5ca3c55e1c2.gif)
- ### A Look in detail
  - #### Search Suggestion Drop Down :
      _Achieved by placing an **absolute positioned div**_
      <div align="center">
      
      ![suggestion123](https://user-images.githubusercontent.com/45242072/57092190-b543ea80-6d02-11e9-954e-d0169758af58.gif)
      
      </div>
      
    - #### Buttons Animations: 
      _Achieved by placing a **::before pseudo element** right ontop of the button anchor text. On hover, the pseudo element expands and fills it's parent_
      
      <div align="center">
      
       ![menu](https://user-images.githubusercontent.com/45242072/57092794-191ae300-6d04-11e9-8cab-6f7dfaf8f19c.gif)
       
      </div>
     
    - #### Hover Drop-Downs
        _Achieved by placing an **absolute positioned div**_ straight after each element. // <a href="https://www.w3schools.com/css/css_combinators.asp" target="_blank">*adjacent siblings*</a>
           
      <div align="center">
      
       ![drop_downs](https://user-images.githubusercontent.com/45242072/57093324-75cacd80-6d05-11e9-84ae-216d67c741f9.gif)
       
      </div>
      
## NPM Dev Packages:
```json
 "devDependencies": {
    "autoprefixer": "^7.1.4",
    "concat": "^1.0.3",
    "node-sass": "^4.5.3",
    "npm-run-all": "^4.1.1",
    "postcss-cli": "^4.1.1"
  }
```
## NPM Scripts:
```json
  "scripts": {
      "watch:sass": "node-sass sass/main.scss css/style.css -w",
      "devserver": "live-server",
      "start": "npm-run-all --parallel devserver watch:sass",
      "compile:sass": "node-sass sass/main.scss css/style.comp.css",
      "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.comp.css -o css/style.prefix.css",
      "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
      "build:css": "npm-run-all compile:sass  prefix:css compress:css"
   }
```