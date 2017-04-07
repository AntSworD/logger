
## Different with `koa-logger` - Diy your logger

  The Logger which diy by yourself have to defined a method that name `log` or `info`.

```js
const logger = require('koa-diy-logger')
const Koa = require('koa')
const diyLogger = require('log4js').getLogger();

const app = new Koa()
app.use(logger(diyLogger))
```

# koa-logger

[![npm version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]

 Development style logger middleware for [koa](https://github.com/koajs/koa).

___Notice: `koa-logger@2` supports `koa@2`; if you want to use this module with `koa@1`, please use `koa-logger@1`.___

```
<-- GET /
--> GET / 200 835ms 746b
<-- GET /
--> GET / 200 960ms 1.9kb
<-- GET /users
--> GET /users 200 357ms 922b
<-- GET /users?page=2
--> GET /users?page=2 200 466ms 4.66kb
```

## Installation

```js
$ npm install koa-diy-logger
```

## Example

```js
const logger = require('koa-logger')
const Koa = require('koa')

const app = new Koa()
app.use(logger())
```

## Notes

  Recommended that you `.use()` this middleware near the top
  to "wrap" all subsequent middleware.

## License

  MIT

[npm-image]: https://img.shields.io/npm/v/koa-logger.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/koa-logger
[travis-image]: https://img.shields.io/travis/koajs/logger.svg?style=flat-square
[travis-url]: https://travis-ci.org/koajs/logger
