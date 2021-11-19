# React 17
- babel.min.js https://unpkg.com/@babel/standalone/babel.min.js)
  - Convert ES6 to ES5
  - Convert JSX to JS
- react.development.js (https://unpkg.com/browse/react@17.0.2/umd/react.development.js) (https://unpkg.com/browse/react@17.0.2/umd/react.production.min.js)
  - react core lib
- react-dom.development.js (https://unpkg.com/browse/react-dom@17.0.2/umd/react-dom.development.js) (https://unpkg.com/browse/react-dom@17.0.2/umd/react-dom.production.min.js)
  - react extention lib

## When import above lib, you have to import by a sort:
  - react development.js must be imported before react-dom.development.js. 

## JavaScript statement vs expression
  - Expression: A expression generates value and it can be put to any place where need value.for example: 
    1. a
    2. a+b
    3. demo(1)
    4. arr.map()
    5. function test() { }
  - react statement or code just control direction. forexample:
    1. if () {}
    2. for () {} 
    3. .swith(){case: xxx}  

## Simple component vs complex component
  - Simple component - No state component
  - Complex component - with state component

## 3 features of Component instant object
  1. State
  2. 

# How to use react
1. react framework - create-react-app
2. framework structure: react + webpack + es6 + eslint
## Create project and installation
1. Global installation - npm install -g create-react-app
2. change to your project directory, use following command:
  create-react-app hello-react
3. enter your project directory - cd hello-react
4. start your project - npm start

### Where is the state, where is the method of operating the state.

### React config multiple proxy
- under /src directory, create a js file named setupProxy.js
> const proxy = require('http-proxy-middleware')
  module.exports = function (app){
    app.use(
      proxy('/api1', {//when prefix has /api1, the proxy will be used.
        target: 'http://localhost:5000',
        changeOrigin: true,//Control server will receive the Host value of the request
        pathRewrite: {'^/api1':''}//rewrite request path (Required)
      }),
      proxy('/api2', {
        target: 'http://localhost:5001',
        changeOrigin: true,
        pathRewrite: {'^/api2':''}
      })
    )
  }
