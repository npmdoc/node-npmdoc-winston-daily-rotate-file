# api documentation for  [winston-daily-rotate-file (v1.4.6)](https://github.com/winstonjs/winston-daily-rotate-file#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-winston-daily-rotate-file.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-winston-daily-rotate-file) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-winston-daily-rotate-file.svg)](https://travis-ci.org/npmdoc/node-npmdoc-winston-daily-rotate-file)
#### A transport for winston which logs to a rotating file each day.

[![NPM](https://nodei.co/npm/winston-daily-rotate-file.png?downloads=true)](https://www.npmjs.com/package/winston-daily-rotate-file)

[![apidoc](https://npmdoc.github.io/node-npmdoc-winston-daily-rotate-file/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-winston-daily-rotate-file_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-winston-daily-rotate-file/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-winston-daily-rotate-file/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-winston-daily-rotate-file/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Charlie Robbins",
        "email": "charlie.robbins@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/winstonjs/winston-daily-rotate-file/issues"
    },
    "dependencies": {},
    "description": "A transport for winston which logs to a rotating file each day.",
    "devDependencies": {
        "chai": "3.5.0",
        "eslint": "2.10.2",
        "eslint-config-xo-space": "0.13.0",
        "mkdirp": "0.5.1",
        "mocha": "2.4.5",
        "moment": "2.13.0",
        "rimraf": "2.5.2",
        "timekeeper": "^0.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "f204b6ada19a5386fdf52fe997d8e10e43ff7788",
        "tarball": "https://registry.npmjs.org/winston-daily-rotate-file/-/winston-daily-rotate-file-1.4.6.tgz"
    },
    "eslintConfig": {
        "extends": "xo-space",
        "env": {
            "node": true,
            "mocha": true
        }
    },
    "gitHead": "6cb4c688c09d4c1ddf5e664825fc108c77e110b6",
    "homepage": "https://github.com/winstonjs/winston-daily-rotate-file#readme",
    "keywords": [
        "winston",
        "daily-rotate-file",
        "log-rotate",
        "logrotate"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "indexzero",
            "email": "charlie.robbins@gmail.com"
        },
        {
            "name": "mattberther",
            "email": "matt@berther.io"
        }
    ],
    "name": "winston-daily-rotate-file",
    "optionalDependencies": {},
    "peerDependencies": {
        "winston": "2.x"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/winstonjs/winston-daily-rotate-file.git"
    },
    "scripts": {
        "postversion": "git push && git push --tags && npm publish",
        "preversion": "npm test",
        "test": "mocha && eslint ."
    },
    "version": "1.4.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module winston-daily-rotate-file](#apidoc.module.winston-daily-rotate-file)
1.  [function <span class="apidocSignatureSpan">winston-daily-rotate-file.</span>super_ (options)](#apidoc.element.winston-daily-rotate-file.super_)
1.  object <span class="apidocSignatureSpan">winston-daily-rotate-file.</span>super_.prototype

#### [module winston-daily-rotate-file.super_](#apidoc.module.winston-daily-rotate-file.super_)
1.  [function <span class="apidocSignatureSpan">winston-daily-rotate-file.</span>super_ ()](#apidoc.element.winston-daily-rotate-file.super_.super_)

#### [module winston-daily-rotate-file.super_.prototype](#apidoc.module.winston-daily-rotate-file.super_.prototype)
1.  [function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>formatQuery (query)](#apidoc.element.winston-daily-rotate-file.super_.prototype.formatQuery)
1.  [function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>formatResults (results, options)](#apidoc.element.winston-daily-rotate-file.super_.prototype.formatResults)
1.  [function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>logException (msg, meta, callback)](#apidoc.element.winston-daily-rotate-file.super_.prototype.logException)
1.  [function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>normalizeQuery (options)](#apidoc.element.winston-daily-rotate-file.super_.prototype.normalizeQuery)



# <a name="apidoc.module.winston-daily-rotate-file"></a>[module winston-daily-rotate-file](#apidoc.module.winston-daily-rotate-file)

#### <a name="apidoc.element.winston-daily-rotate-file.super_"></a>[function <span class="apidocSignatureSpan">winston-daily-rotate-file.</span>super_ (options)](#apidoc.element.winston-daily-rotate-file.super_)
- description and source-code
```javascript
super_ = function (options) {
  events.EventEmitter.call(this);

  options        = options        || {};
  this.silent    = options.silent || false;
  this.raw       = options.raw    || false;
  this.name      = options.name   || this.name;
  this.formatter = options.formatter;

  //
  // Do not set a default level. When 'level' is falsey on any
  // 'Transport' instance, any 'Logger' instance uses the
  // configured level (instead of the Transport level)
  //
  this.level = options.level;

  this.handleExceptions = options.handleExceptions || false;
  this.exceptionsLevel  = options.exceptionsLevel || 'error';
  this.humanReadableUnhandledException = options.humanReadableUnhandledException || false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.winston-daily-rotate-file.super_"></a>[module winston-daily-rotate-file.super_](#apidoc.module.winston-daily-rotate-file.super_)

#### <a name="apidoc.element.winston-daily-rotate-file.super_.super_"></a>[function <span class="apidocSignatureSpan">winston-daily-rotate-file.</span>super_ ()](#apidoc.element.winston-daily-rotate-file.super_.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.winston-daily-rotate-file.super_.prototype"></a>[module winston-daily-rotate-file.super_.prototype](#apidoc.module.winston-daily-rotate-file.super_.prototype)

#### <a name="apidoc.element.winston-daily-rotate-file.super_.prototype.formatQuery"></a>[function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>formatQuery (query)](#apidoc.element.winston-daily-rotate-file.super_.prototype.formatQuery)
- description and source-code
```javascript
formatQuery = function (query) {
  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.winston-daily-rotate-file.super_.prototype.formatResults"></a>[function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>formatResults (results, options)](#apidoc.element.winston-daily-rotate-file.super_.prototype.formatResults)
- description and source-code
```javascript
formatResults = function (results, options) {
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.winston-daily-rotate-file.super_.prototype.logException"></a>[function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>logException (msg, meta, callback)](#apidoc.element.winston-daily-rotate-file.super_.prototype.logException)
- description and source-code
```javascript
logException = function (msg, meta, callback) {
  var self = this,
      called;

  if (this.silent) {
    return callback();
  }

  function onComplete () {
    if (!called) {
      called = true;
      self.removeListener('logged', onComplete);
      self.removeListener('error', onComplete);
      callback();
    }
  }

  this.once('logged', onComplete);
  this.once('error', onComplete);
  this.log(self.exceptionsLevel, msg, meta, function () { });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.winston-daily-rotate-file.super_.prototype.normalizeQuery"></a>[function <span class="apidocSignatureSpan">winston-daily-rotate-file.super_.prototype.</span>normalizeQuery (options)](#apidoc.element.winston-daily-rotate-file.super_.prototype.normalizeQuery)
- description and source-code
```javascript
normalizeQuery = function (options) {
  //
  // Use options similar to loggly.
  // [See Loggly Search API](http://wiki.loggly.com/retrieve_events#optional)
  //

  options = options || {};

  // limit
  options.rows = options.rows || options.limit || 10;

  // starting row offset
  options.start = options.start || 0;

  // now
  options.until = options.until || new Date;
  if (typeof options.until !== 'object') {
    options.until = new Date(options.until);
  }

  // now - 24
  options.from = options.from || (options.until - (24 * 60 * 60 * 1000));
  if (typeof options.from !== 'object') {
    options.from = new Date(options.from);
  }


  // 'asc' or 'desc'
  options.order = options.order || 'desc';

  // which fields to select
  options.fields = options.fields;

  return options;
}
```
- example usage
```shell
...
if (typeof options === 'function') {
  callback = options;
  options = {};
}

// TODO when maxfilesize rotate occurs
var file = path.join(this.dirname, this._getFilename());
options = this.normalizeQuery(options);
var buff = '';
var results = [];
var row = 0;

var stream = fs.createReadStream(file, {
  encoding: 'utf8'
});
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
