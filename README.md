# Hyperapp 2.0 PWA/SPA boilerplate
*Hyperapp starter kit with development on steroids*  

## Installation: 
```
# Clone project
git clone https://github.com/loteoo/hyperapp-boilerplate.git

cd hyperapp-boilerplate

npm install     # Install dependencies
npm start       # Dev server + live reload
```

```
npm run build   # Build for production
```


 
## In a nutshell

JS up to ES8 with JSX  
PostCSS with rucksack enhancements  
Code generators included for common use cases  
Uses Parcel for compilation, dev server, watcher with live reload, hot modules...  



## File structure
Proposed folder structure as your project grows. Adapt it to your needs.

```
├── _templates/                       # Hygen code generators
├── public/                           # Compiled static files (parcel output)
├── src/                              # Application source code
│   ├── app/                          # Global app files
│   │   ├── components/               # Vertically separated components
│   │   │   ├── common/               # Utility components, ex: text input, modal container, etc.
│   │   │   ├── pages/                # Pages are top level components, generally triggered by a router
│   │   │   ├── {ComponentName}/      # Advanced component with multiple files
│   │   │   │   ├── index.jsx
│   │   │   │   ├── actions.js
│   │   │   │   ├── style.css
│   │   │   │   └── other.png
│   │   │   └── {ComponentName}.jsx   # Simple component
│   │   ├── actions.js                # Global actions
│   │   ├── index.js                  # Hyperapp instantiation
│   │   ├── init.js                   # Initial app state
│   │   ├── style.css                 # Global css
│   │   ├── utils.js                  # Utility functions
│   │   └── view.jsx                  # Root view
│   ├── assets/                       # Global application assets (favicon, fonts...)
│   ├── index.html                    # Parcel entry
│   ├── ...
├── ...
...
```




## Code generators
Generate new Hyperapp components like this:
```
.\node_modules\.bin\hygen component new --name 'my component'
.\node_modules\.bin\hygen complex-component new --name 'advanced component'
```
Available generators are located in the _templates folder  
If you have hygen installed globally, which I recommend, you can do this instead: 
```
hygen component new --name 'my component'
```
 
http://www.hygen.io/







## CSS 
PostCSS is ready to go, with nested syntax & rucksack css enhancements.  
https://www.rucksackcss.org/

An opinionated, 'best practices' css reset is loaded in the starterkit as well  
https://github.com/csstools/sanitize.css

A starter "theme" is also pre-written for you to edit in /src/app/style.css





### Hyperapp 2.0 TLDR:

State => Data of your app, usually a javascript object  
View => Pure function that maps the state to a DOM representation (called virtual DOM)  
Actions => Pure functions that take in a state, some params, and returns a new state  
Subscribtions => Fancy event listeners that are aware of the state  
Effects => Functions in wich you do encapsulate side effects, to interact with the outside world.  

Use functional programming to describe an application  
and let Hyperapp bring it to life  

https://github.com/jorgebucaran/hyperapp/pull/726  

> Please correct me if you disagree with this TLDR [😈](https://meta.wikimedia.org/wiki/Cunningham%27s_Law)  



### To-do list demo app:
Basic CRUD actions with hyperapp 2.0  
https://github.com/loteoo/hyperapp-todolist


> *Disclaimer:*  
This is an opinionated setup fine-tuned to how 
I personally build webapps with hyperapp.  
If you're getting started with Hyperapp or with 
JS in general, you can progressively use it's features 
as you learn and stick with what you know.


---  


https://github.com/loteoo/hyperapp-boilerplate

