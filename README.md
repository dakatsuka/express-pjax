[![build status](https://secure.travis-ci.org/dakatsuka/express-pjax.png)](http://travis-ci.org/dakatsuka/express-pjax)
# express-pjax

Express middleware for Pjax.

## Installation

```
npm install express-pjax
```

## Usage

If you use `res.renderPjax` method, the request of pjax will be handled automatically.

```javascript
var express = require('express');
var pjax    = require('express-pjax');
var app     = express.createServer();

app.configure(function() {
  app.use(pjax());
  // -- snip --
});

app.get('/', function(req, res) {
  res.renderPjax('index', { locals: { hello: "Hello World!" } });
});

app.get('/foo', function(req, res) {
  res.renderPjax('foo');
});
```

## DEMO

https://github.com/abdelsaid/express-pjax-demo

## TODO

* Support redirect.

## Copyright

Copyright (C) 2011 Dai Akatsuka, released under the MIT License.
