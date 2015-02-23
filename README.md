ngAA
=======
[![Build Status](https://travis-ci.org/lykmapipo/ngAA.svg?branch=master)](https://travis-ci.org/lykmapipo/ngAA)

[![Tips](https://img.shields.io/gratipay/lykmapipo.svg)](https://gratipay.com/lykmapipo/)

[![Support via Gratipay](https://cdn.rawgit.com/gratipay/gratipay-badge/2.3.0/dist/gratipay.svg)](https://gratipay.com/lykmapipo/)

DRY authentication and authorization for angular and ui-router.

*Note: ngAA works only with [ui-router](https://github.com/angular-ui/ui-router)*

## Dependencies
- [angular](https://github.com/angular/angular.js)
- [angular-ui-router](https://github.com/angular-ui/ui-router)
- [angular-jwt](https://github.com/auth0/angular-jwt)
- [ngstorage](https://github.com/gsklee/ngStorage)

## Install
```sh
$ bower install --save ngAA
```
## Usage
- **Include `ngAA` into your app index.html**
```html
<!doctype html>
<html ng-app="yourApp">
<head>
    ...
</head>
<body>
    ...

    <!-- build:js(.) scripts/vendor.js -->
    <!-- bower:js -->
    <script src="bower_components/angular/angular.js"></script>
    <script src="bower_components/angular-ui-router/release/angular-ui-router.js"></script>
    <script src="bower_components/angular-jwt/dist/angular-jwt.js"></script>
    <script src="bower_components/ngstorage/ngStorage.js"></script>
    <script src="bower_components/ngAA/dist/ngAA.js"></script>
    <!-- endbower -->
    <!-- endbuild -->

    <!-- build:js({.tmp,app}) scripts/yourApp.js -->
    <script src="scripts/app.js"></script>
    <!-- endbuild -->
</body>
</html>
```

- **Require `ngAA` module into your angular application or module**
```js
angular
.module('yourApp',[
'ngAA'
])
config(function($stateProvider, $urlRouterProvider, $authProvider) {
        //configure after user signin redirect state
        $authProvider.afterSigninRedirectTo = 'contact';
        //configure after user signout redirect state
        $authProvider.afterSignoutRedirectTo = 'main';
});
```

## Testing

* Clone this repository

* Install all development dependencies

```sh
$ npm install && bower install
```

* Then run test

```sh
$ npm test
```

## Contribute

Fork this repo and push in your ideas. 
Do not forget to add a bit of test(s) of what value you adding.

## Licence

Copyright (c) 2015 lykmapipo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.