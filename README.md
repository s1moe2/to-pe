# to-pe

Simple module to bind await-to-js with parse-error modules as described in [this article](https://codeburst.io/build-a-rest-api-for-node-mysql-2018-jwt-6957bcfc7ac9).


## Pre-requisites
The pre-requisites from [await-to-js](https://github.com/scopsy/await-to-js#pre-requisites):

> You need to use Node 7.6 (or later) or an ES7 transpiler in order to use async/await functionality. You can use babel or typescript for that.

## Install

```sh
npm i -s to-pe
```

## Usage
Use it just like in await-to-js but now the error will be a parse error object as described in [parse-error](https://github.com/watilde/parse-error)

```js
const to = require('to-pe');

[ err, user ] = await to(UserModel.findById(1));
if(!user) return cb('No user found');
```