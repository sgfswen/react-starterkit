# Starterkit

This react starterkit provides a prepared development environment based on [gulp](https://github.com/gulpjs/gulp), [stylus](https://github.com/LearnBoost/stylus) and [webpack](https://github.com/webpack/webpack). It also includes [Reflux](https://github.com/spoike/refluxjs) and [React-Router](https://github.com/rackt/react-route).

## Installation

Install all dependencies. 

```
$ npm install
```


## Development

Builds the application and starts a webserver with livereload. By default the webserver starts at port 1337.
You can define a port with `$ gulp --port 3333`.

```
$ gulp
```

**Javascript**

Javascript entry file: `app/scripts/main.js` <br />
We are using Reflux, which is an implemantion of the [Flux Architecture](http://facebook.github.io/flux/docs/overview.html). Basically it's about how components communicate with each other. If you want to read more about Reflux, check out the readme of the [reflux git repo](https://github.com/spoike/refluxjs). 

**CSS**

CSS entry file: `app/stylus/main.styl`<br />

If you want to use third-party CSS you just include it via `@import 'path/to/your/third-party-styles.css'` at the top of the main.styl file.



## Build

Builds a minified version of the application in the dist folder.

```
$ gulp build --type production
```

## Webpack Hints

We use the jsx-loader in order to load .jsx files via webpack.

### Imports Loader

If you want to use plugins for a certain library, that does not require dependencies you can use the [imports loader](http://webpack.github.io/docs/shimming-modules.html#imports-loader). Here the file 'awesome-plugin.js' expects a global variable called jQuery. We can just import that variable via ```jQuery=path/to/jQuery```.

Install the imports loader via:

```
npm install --save imports-loader
```
You can use it in your code like:

```
require("imports?jQuery=../bower_components/jquery/dist/jquery!./awesome-plugin.js");
```




###Requirements
* node
* npm
* bower
* gulp
