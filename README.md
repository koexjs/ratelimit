# koa-rate-limit

[![NPM version](https://img.shields.io/npm/v/@zcorky/koa-rate-limit.svg?style=flat)](https://www.npmjs.com/package/@zcorky/koa-rate-limit)
[![Coverage Status](https://img.shields.io/coveralls/zcorky/koa-rate-limit.svg?style=flat)](https://coveralls.io/r/zcorky/koa-rate-limit)
[![Dependencies](https://david-dm.org/@zcorky/koa-rate-limit/status.svg)](https://david-dm.org/@zcorky/koa-rate-limit)
[![Build Status](https://travis-ci.com/zcorky/koa-rate-limit.svg?branch=master)](https://travis-ci.com/zcorky/koa-rate-limit)
![license](https://img.shields.io/github/license/zcorky/koa-rate-limit.svg)
[![issues](https://img.shields.io/github/issues/zcorky/koa-rate-limit.svg)](https://github.com/zcorky/koa-rate-limit/issues)

> Deep Diff & Patch in js, maybe data visition timeline json data is common for use.
> Diff => CREATE / UPDATE / DELETE / UNCHANGE Data.
> Patch => Immutable Philosophy Data.

### Install

```
$ npm install @zcorky/koa-rate-limit
```

### Usage

```javascript
// See more in test
import ratelimit from '@zcorky/koa-rate-limit';

import * as Koa from 'koa';
const app = new Koa();
app.use(ratelimit());
app.use(async (ctx) => {
  if (ctx.path === '/') {
    ctx.body = 'hello, world';
  } else if (ctx.path === '/json') {
    ctx.body = {
      name: 'name',
      value: 'value',
    };
  }
});

app.listen(8000, '0.0.0.0', () => {
  console.log('koa server start');
});
```

### Related
* [ratelimit](https://github.com/koajs/ratelimit)