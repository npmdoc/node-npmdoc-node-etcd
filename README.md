# api documentation for  [node-etcd (v5.0.3)](https://github.com/stianeikeland/node-etcd#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-etcd.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-etcd) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-etcd.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-etcd)
#### etcd library for node.js (etcd v2 api)

[![NPM](https://nodei.co/npm/node-etcd.png?downloads=true)](https://www.npmjs.com/package/node-etcd)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-etcd/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-etcd_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-etcd/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-etcd/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-etcd/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/stianeikeland/node-etcd/issues"
    },
    "dependencies": {
        "deasync": "0.1.7",
        "request": "2.60.0",
        "underscore": "1.8.2",
        "url-parse": "1.0.5"
    },
    "description": "etcd library for node.js (etcd v2 api)",
    "devDependencies": {
        "coffee-script": "1.9.1",
        "mocha": "2.1.0",
        "nock": "2.17.0",
        "should": "5.0.1",
        "simple-mock": "0.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "8b616da4689b5456ca686b24294214330c471bf8",
        "tarball": "https://registry.npmjs.org/node-etcd/-/node-etcd-5.0.3.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "fea875005d654e06aba2e1374085d7a57448420c",
    "homepage": "https://github.com/stianeikeland/node-etcd#readme",
    "keywords": [
        "etcd",
        "raft"
    ],
    "licenses": [
        {
            "type": "BSD 3-Clause",
            "url": "http://opensource.org/licenses/BSD-3-Clause"
        }
    ],
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "stiane",
            "email": "stian@eikeland.se"
        }
    ],
    "name": "node-etcd",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/stianeikeland/node-etcd.git"
    },
    "scripts": {
        "build": "coffee --bare --compile --output lib/ src/*.coffee",
        "postpublish": "rm -rf lib",
        "prepublish": "coffee --bare --compile --output lib/ src/*.coffee",
        "test": "mocha --compilers coffee:coffee-script/register test/",
        "watch": "mocha --compilers coffee:coffee-script/register --watch"
    },
    "version": "5.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-etcd](#apidoc.module.node-etcd)
1.  [function <span class="apidocSignatureSpan">node-etcd.</span>client (hosts, options1, sslopts)](#apidoc.element.node-etcd.client)
1.  [function <span class="apidocSignatureSpan">node-etcd.</span>watcher (etcd, key, index, options)](#apidoc.element.node-etcd.watcher)
1.  object <span class="apidocSignatureSpan">node-etcd.</span>client.prototype
1.  object <span class="apidocSignatureSpan">node-etcd.</span>watcher.prototype

#### [module node-etcd.client](#apidoc.module.node-etcd.client)
1.  [function <span class="apidocSignatureSpan">node-etcd.</span>client (hosts, options1, sslopts)](#apidoc.element.node-etcd.client.client)

#### [module node-etcd.client.prototype](#apidoc.module.node-etcd.client.prototype)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_doRequest (options, reqRespHandler)](#apidoc.element.node-etcd.client.prototype._doRequest)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_error (token, callback)](#apidoc.element.node-etcd.client.prototype._error)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_handleResponse (err, resp, body, callback)](#apidoc.element.node-etcd.client.prototype._handleResponse)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_isHttpError (err, resp)](#apidoc.element.node-etcd.client.prototype._isHttpError)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_isPossibleLeaderElection (errors)](#apidoc.element.node-etcd.client.prototype._isPossibleLeaderElection)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_multiserverHelper (servers, options, token, callback)](#apidoc.element.node-etcd.client.prototype._multiserverHelper)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_retry (token, options, callback)](#apidoc.element.node-etcd.client.prototype._retry)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_shouldRetry (token)](#apidoc.element.node-etcd.client.prototype._shouldRetry)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_waitTime (retries)](#apidoc.element.node-etcd.client.prototype._waitTime)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>delete (options, callback)](#apidoc.element.node-etcd.client.prototype.delete)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>execute (method, options, callback)](#apidoc.element.node-etcd.client.prototype.execute)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>get (options, callback)](#apidoc.element.node-etcd.client.prototype.get)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>patch (options, callback)](#apidoc.element.node-etcd.client.prototype.patch)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>post (options, callback)](#apidoc.element.node-etcd.client.prototype.post)
1.  [function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>put (options, callback)](#apidoc.element.node-etcd.client.prototype.put)

#### [module node-etcd.watcher](#apidoc.module.node-etcd.watcher)
1.  boolean <span class="apidocSignatureSpan">node-etcd.watcher.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">node-etcd.</span>watcher (etcd, key, index, options)](#apidoc.element.node-etcd.watcher.watcher)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.</span>EventEmitter ()](#apidoc.element.node-etcd.watcher.EventEmitter)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.</span>init ()](#apidoc.element.node-etcd.watcher.init)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.</span>listenerCount (emitter, type)](#apidoc.element.node-etcd.watcher.listenerCount)
1.  number <span class="apidocSignatureSpan">node-etcd.watcher.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">node-etcd.watcher.</span>__super__

#### [module node-etcd.watcher.prototype](#apidoc.module.node-etcd.watcher.prototype)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_error (err)](#apidoc.element.node-etcd.watcher.prototype._error)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_missingValue (headers)](#apidoc.element.node-etcd.watcher.prototype._missingValue)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_respHandler (err, val, headers)](#apidoc.element.node-etcd.watcher.prototype._respHandler)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_resync (err)](#apidoc.element.node-etcd.watcher.prototype._resync)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_retry ()](#apidoc.element.node-etcd.watcher.prototype._retry)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_unexpectedData (val, headers)](#apidoc.element.node-etcd.watcher.prototype._unexpectedData)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_valueChanged (val, headers)](#apidoc.element.node-etcd.watcher.prototype._valueChanged)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_watch ()](#apidoc.element.node-etcd.watcher.prototype._watch)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>constructor (etcd, key, index, options)](#apidoc.element.node-etcd.watcher.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>stop ()](#apidoc.element.node-etcd.watcher.prototype.stop)



# <a name="apidoc.module.node-etcd"></a>[module node-etcd](#apidoc.module.node-etcd)

#### <a name="apidoc.element.node-etcd.client"></a>[function <span class="apidocSignatureSpan">node-etcd.</span>client (hosts, options1, sslopts)](#apidoc.element.node-etcd.client)
- description and source-code
```javascript
function Client(hosts, options1, sslopts) {
  this.hosts = hosts;
  this.options = options1;
  this.sslopts = sslopts;
  this._shouldRetry = bind(this._shouldRetry, this);
  this._retry = bind(this._retry, this);
  this._multiserverHelper = bind(this._multiserverHelper, this);
  this["delete"] = bind(this["delete"], this);
  this.patch = bind(this.patch, this);
  this.post = bind(this.post, this);
  this.get = bind(this.get, this);
  this.put = bind(this.put, this);
  this.execute = bind(this.execute, this);
  this.syncmsg = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-etcd.watcher"></a>[function <span class="apidocSignatureSpan">node-etcd.</span>watcher (etcd, key, index, options)](#apidoc.element.node-etcd.watcher)
- description and source-code
```javascript
function Watcher(etcd, key, index, options) {
  this.etcd = etcd;
  this.key = key;
  this.index = index != null ? index : null;
  this.options = options != null ? options : {};
  this._retry = bind(this._retry, this);
  this._respHandler = bind(this._respHandler, this);
  this._resync = bind(this._resync, this);
  this._unexpectedData = bind(this._unexpectedData, this);
  this._valueChanged = bind(this._valueChanged, this);
  this._missingValue = bind(this._missingValue, this);
  this._error = bind(this._error, this);
  this._watch = bind(this._watch, this);
  this.stop = bind(this.stop, this);
  this.stopped = false;
  this.retryAttempts = 0;
  this._watch();
}
```
- example usage
```shell
...

'''javascript
etcd.watch("key");
etcd.watch("key", console.log);
'''

The watch command is pretty low level, it does not handle reconnects or
timeouts (Etcd will disconnect you after 5 minutes). Use the '.watcher()' below
if you do not wish to handle this yourself.

### .watchIndex(key, index, [options], callback)

This is a convenience method for get with '{wait: true, waitIndex: index}'.

'''javascript
...
```



# <a name="apidoc.module.node-etcd.client"></a>[module node-etcd.client](#apidoc.module.node-etcd.client)

#### <a name="apidoc.element.node-etcd.client.client"></a>[function <span class="apidocSignatureSpan">node-etcd.</span>client (hosts, options1, sslopts)](#apidoc.element.node-etcd.client.client)
- description and source-code
```javascript
function Client(hosts, options1, sslopts) {
  this.hosts = hosts;
  this.options = options1;
  this.sslopts = sslopts;
  this._shouldRetry = bind(this._shouldRetry, this);
  this._retry = bind(this._retry, this);
  this._multiserverHelper = bind(this._multiserverHelper, this);
  this["delete"] = bind(this["delete"], this);
  this.patch = bind(this.patch, this);
  this.post = bind(this.post, this);
  this.get = bind(this.get, this);
  this.put = bind(this.put, this);
  this.execute = bind(this.execute, this);
  this.syncmsg = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-etcd.client.prototype"></a>[module node-etcd.client.prototype](#apidoc.module.node-etcd.client.prototype)

#### <a name="apidoc.element.node-etcd.client.prototype._doRequest"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_doRequest (options, reqRespHandler)](#apidoc.element.node-etcd.client.prototype._doRequest)
- description and source-code
```javascript
_doRequest = function (options, reqRespHandler) {
  return request(options, reqRespHandler);
}
```
- example usage
```shell
...
      headers: headers
    };
  };
})(this);
if (options.synchronous === true) {
  callback = syncRespHandler;
}
req = this._doRequest(options, reqRespHandler);
token.setRequest(req);
if (options.synchronous === true && options.syncdone === void 0) {
  options.syncdone = false;
  while (!options.syncdone) {
    deasync.runLoopOnce();
  }
  delete options.syncdone;
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._error"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_error (token, callback)](#apidoc.element.node-etcd.client.prototype._error)
- description and source-code
```javascript
_error = function (token, callback) {
  var error;
  error = new Error('All servers returned error');
  error.errors = token.errors;
  error.retries = token.retries;
  if (callback) {
    return callback(error);
  }
}
```
- example usage
```shell
...
if (token.isAborted()) {
  return;
}
if (host == null) {
  if (this._shouldRetry(token)) {
    return this._retry(token, options, callback);
  }
  return this._error(token, callback);
}
reqRespHandler = (function(_this) {
  return function(err, resp, body) {
    if (token.isAborted()) {
      return;
    }
    if (_this._isHttpError(err, resp)) {
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._handleResponse"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_handleResponse (err, resp, body, callback)](#apidoc.element.node-etcd.client.prototype._handleResponse)
- description and source-code
```javascript
_handleResponse = function (err, resp, body, callback) {
  var error;
  if (callback == null) {
    return;
  }
  if ((body != null ? body.errorCode : void 0) != null) {
    error = new Error((body != null ? body.message : void 0) || 'Etcd error');
    error.errorCode = body.errorCode;
    error.error = body;
    return callback(error, "", (resp != null ? resp.headers : void 0) || {});
  } else {
    return callback(null, body, (resp != null ? resp.headers : void 0) || {});
  }
}
```
- example usage
```shell
...
        httpstatus: resp != null ? resp.statusCode : void 0,
        httpbody: resp != null ? resp.body : void 0,
        response: resp,
        timestamp: new Date()
      });
      return _this._multiserverHelper(_.rest(servers), options, token, callback);
    }
    return _this._handleResponse(err, resp, body, callback);
  };
})(this);
syncRespHandler = (function(_this) {
  return function(err, body, headers) {
    options.syncdone = true;
    return _this.syncmsg = {
      err: err,
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._isHttpError"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_isHttpError (err, resp)](#apidoc.element.node-etcd.client.prototype._isHttpError)
- description and source-code
```javascript
_isHttpError = function (err, resp) {
  return err || (((resp != null ? resp.statusCode : void 0) != null) && resp.statusCode >= 500);
}
```
- example usage
```shell
...
  return this._error(token, callback);
}
reqRespHandler = (function(_this) {
  return function(err, resp, body) {
    if (token.isAborted()) {
      return;
    }
    if (_this._isHttpError(err, resp)) {
      token.errors.push({
        server: host,
        httperror: err,
        httpstatus: resp != null ? resp.statusCode : void 0,
        httpbody: resp != null ? resp.body : void 0,
        response: resp,
        timestamp: new Date()
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._isPossibleLeaderElection"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_isPossibleLeaderElection (errors)](#apidoc.element.node-etcd.client.prototype._isPossibleLeaderElection)
- description and source-code
```javascript
_isPossibleLeaderElection = function (errors) {
  var checkError;
  checkError = function(e) {
    var ref, ref1, ref2, ref3;
    return ((ref = e != null ? (ref1 = e.httperror) != null ? ref1.code : void 0 : void 0) === 'ECONNREFUSED' || ref === 'ECONNRESET
') || ((ref2 = e != null ? (ref3 = e.httpbody) != null ? ref3.errorCode : void 0 : void 0) === 300 || ref2 === 301) || /Not current
 leader/.test(e != null ? e.httpbody : void 0);
  };
  return (errors != null) && _.every(errors, checkError);
}
```
- example usage
```shell
...
  if (process.env.RUNNING_UNIT_TESTS === 'true') {
    return 1;
  }
  return 100 * Math.pow(16, retries);
};

Client.prototype._shouldRetry = function(token) {
  return token.retries < token.maxRetries && this._isPossibleLeaderElection(token.errors);
};

Client.prototype._error = function(token, callback) {
  var error;
  error = new Error('All servers returned error');
  error.errors = token.errors;
  error.retries = token.retries;
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._multiserverHelper"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_multiserverHelper (servers, options, token, callback)](#apidoc.element.node-etcd.client.prototype._multiserverHelper)
- description and source-code
```javascript
_multiserverHelper = function (servers, options, token, callback) {
  var host, req, reqRespHandler, syncRespHandler;
  host = _.first(servers);
  options.url = "" + host + options.path;
  if (token.isAborted()) {
    return;
  }
  if (host == null) {
    if (this._shouldRetry(token)) {
      return this._retry(token, options, callback);
    }
    return this._error(token, callback);
  }
  reqRespHandler = (function(_this) {
    return function(err, resp, body) {
      if (token.isAborted()) {
        return;
      }
      if (_this._isHttpError(err, resp)) {
        token.errors.push({
          server: host,
          httperror: err,
          httpstatus: resp != null ? resp.statusCode : void 0,
          httpbody: resp != null ? resp.body : void 0,
          response: resp,
          timestamp: new Date()
        });
        return _this._multiserverHelper(_.rest(servers), options, token, callback);
      }
      return _this._handleResponse(err, resp, body, callback);
    };
  })(this);
  syncRespHandler = (function(_this) {
    return function(err, body, headers) {
      options.syncdone = true;
      return _this.syncmsg = {
        err: err,
        body: body,
        headers: headers
      };
    };
  })(this);
  if (options.synchronous === true) {
    callback = syncRespHandler;
  }
  req = this._doRequest(options, reqRespHandler);
  token.setRequest(req);
  if (options.synchronous === true && options.syncdone === void 0) {
    options.syncdone = false;
    while (!options.syncdone) {
      deasync.runLoopOnce();
    }
    delete options.syncdone;
    return this.syncmsg;
  } else {
    return req;
  }
}
```
- example usage
```shell
...
  var opt, servers, syncResp, token;
  opt = _.defaults(_.clone(options), this.options, defaultRequestOptions, {
    method: method
  });
  opt.clientOptions = _.defaults(opt.clientOptions, defaultClientOptions);
  servers = _.shuffle(this.hosts);
  token = new CancellationToken(servers, opt.clientOptions.maxRetries);
  syncResp = this._multiserverHelper(servers, opt, token, callback);
  if (options.synchronous === true) {
    return syncResp;
  } else {
    return token;
  }
};
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._retry"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_retry (token, options, callback)](#apidoc.element.node-etcd.client.prototype._retry)
- description and source-code
```javascript
_retry = function (token, options, callback) {
  var doRetry, waitTime;
  doRetry = (function(_this) {
    return function() {
      return _this._multiserverHelper(token.servers, options, token, callback);
    };
  })(this);
  waitTime = this._waitTime(token.retries);
  token.retries += 1;
  return setTimeout(doRetry, waitTime);
}
```
- example usage
```shell
...
host = _.first(servers);
options.url = "" + host + options.path;
if (token.isAborted()) {
  return;
}
if (host == null) {
  if (this._shouldRetry(token)) {
    return this._retry(token, options, callback);
  }
  return this._error(token, callback);
}
reqRespHandler = (function(_this) {
  return function(err, resp, body) {
    if (token.isAborted()) {
      return;
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._shouldRetry"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_shouldRetry (token)](#apidoc.element.node-etcd.client.prototype._shouldRetry)
- description and source-code
```javascript
_shouldRetry = function (token) {
  return token.retries < token.maxRetries && this._isPossibleLeaderElection(token.errors);
}
```
- example usage
```shell
...
var host, req, reqRespHandler, syncRespHandler;
host = _.first(servers);
options.url = "" + host + options.path;
if (token.isAborted()) {
  return;
}
if (host == null) {
  if (this._shouldRetry(token)) {
    return this._retry(token, options, callback);
  }
  return this._error(token, callback);
}
reqRespHandler = (function(_this) {
  return function(err, resp, body) {
    if (token.isAborted()) {
...
```

#### <a name="apidoc.element.node-etcd.client.prototype._waitTime"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>_waitTime (retries)](#apidoc.element.node-etcd.client.prototype._waitTime)
- description and source-code
```javascript
_waitTime = function (retries) {
  if (process.env.RUNNING_UNIT_TESTS === 'true') {
    return 1;
  }
  return 100 * Math.pow(16, retries);
}
```
- example usage
```shell
...
Client.prototype._retry = function(token, options, callback) {
  var doRetry, waitTime;
  doRetry = (function(_this) {
    return function() {
      return _this._multiserverHelper(token.servers, options, token, callback);
    };
  })(this);
  waitTime = this._waitTime(token.retries);
  token.retries += 1;
  return setTimeout(doRetry, waitTime);
};

Client.prototype._waitTime = function(retries) {
  if (process.env.RUNNING_UNIT_TESTS === 'true') {
    return 1;
...
```

#### <a name="apidoc.element.node-etcd.client.prototype.delete"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>delete (options, callback)](#apidoc.element.node-etcd.client.prototype.delete)
- description and source-code
```javascript
delete = function (options, callback) {
  return this.execute("DELETE", options, callback);
}
```
- example usage
```shell
...
etcd.del("key/", { recursive: true }, console.log);
'''

Available options include:

- 'recursive' (bool, delete recursively)

Alias: '.delete()'

### .compareAndDelete(key, oldvalue, [options], [callback])

Convenience method for test and delete (delete with {prevValue: oldvalue})

'''javascript
etcd.compareAndDelete("key", "oldvalue");
...
```

#### <a name="apidoc.element.node-etcd.client.prototype.execute"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>execute (method, options, callback)](#apidoc.element.node-etcd.client.prototype.execute)
- description and source-code
```javascript
execute = function (method, options, callback) {
  var opt, servers, syncResp, token;
  opt = _.defaults(_.clone(options), this.options, defaultRequestOptions, {
    method: method
  });
  opt.clientOptions = _.defaults(opt.clientOptions, defaultClientOptions);
  servers = _.shuffle(this.hosts);
  token = new CancellationToken(servers, opt.clientOptions.maxRetries);
  syncResp = this._multiserverHelper(servers, opt, token, callback);
  if (options.synchronous === true) {
    return syncResp;
  } else {
    return token;
  }
}
```
- example usage
```shell
...
    return syncResp;
  } else {
    return token;
  }
};

Client.prototype.put = function(options, callback) {
  return this.execute("PUT", options, callback);
};

Client.prototype.get = function(options, callback) {
  return this.execute("GET", options, callback);
};

Client.prototype.post = function(options, callback) {
...
```

#### <a name="apidoc.element.node-etcd.client.prototype.get"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>get (options, callback)](#apidoc.element.node-etcd.client.prototype.get)
- description and source-code
```javascript
get = function (options, callback) {
  return this.execute("GET", options, callback);
}
```
- example usage
```shell
...

## Basic usage

'''javascript
var Etcd = require('node-etcd');
var etcd = new Etcd();
etcd.set("key", "value");
etcd.get("key", console.log);
'''

Callbacks follows the default (error, result) nodejs convention:

'''javascript
function callback(err, res) {
console.log("Error: ", err);
...
```

#### <a name="apidoc.element.node-etcd.client.prototype.patch"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>patch (options, callback)](#apidoc.element.node-etcd.client.prototype.patch)
- description and source-code
```javascript
patch = function (options, callback) {
  return this.execute("PATCH", options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-etcd.client.prototype.post"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>post (options, callback)](#apidoc.element.node-etcd.client.prototype.post)
- description and source-code
```javascript
post = function (options, callback) {
  return this.execute("POST", options, callback);
}
```
- example usage
```shell
...
- 2.1.4 - Don't wait before reconnecting if Etcd server times out our watcher.
- 2.1.3 - Etcd sends an empty response on timeout in recent versions. Parsing
  the empty message caused watcher to emit error. Now it reconnects instead.
- 2.1.2 - Exponential backoff (retry), fix spinning reconnect on error. (@ptte)
- 2.1.1 - Increase request pool.maxSockets to 100
- 2.1.0 - Use proper error objects instead of strings for errors.
- 2.0.10 - Fix error in documentation
- 2.0.9 - Added .post() alias of .create(). Added .compareAndDelete() (for etcd v0.3.0)
- 2.0.8 - Watchers can be canceled. In-order keys using #create(). Raw requests using #raw().
- 2.0.7 - Avoid calling callback if callback not given.
- 2.0.6 - Refactoring, fix responsehandler error.
- 2.0.5 - Undo use of 'x-etcd-index', this refers to global state.
- 2.0.4 - Use 'x-etcd-index' for index when watching a key.
- 2.0.3 - Watcher supports options. Watcher emits etcd action type.
- 2.0.2 - Mkdir and rmdir. Fix watcher for v2 api.
...
```

#### <a name="apidoc.element.node-etcd.client.prototype.put"></a>[function <span class="apidocSignatureSpan">node-etcd.client.prototype.</span>put (options, callback)](#apidoc.element.node-etcd.client.prototype.put)
- description and source-code
```javascript
put = function (options, callback) {
  return this.execute("PUT", options, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-etcd.watcher"></a>[module node-etcd.watcher](#apidoc.module.node-etcd.watcher)

#### <a name="apidoc.element.node-etcd.watcher.watcher"></a>[function <span class="apidocSignatureSpan">node-etcd.</span>watcher (etcd, key, index, options)](#apidoc.element.node-etcd.watcher.watcher)
- description and source-code
```javascript
function Watcher(etcd, key, index, options) {
  this.etcd = etcd;
  this.key = key;
  this.index = index != null ? index : null;
  this.options = options != null ? options : {};
  this._retry = bind(this._retry, this);
  this._respHandler = bind(this._respHandler, this);
  this._resync = bind(this._resync, this);
  this._unexpectedData = bind(this._unexpectedData, this);
  this._valueChanged = bind(this._valueChanged, this);
  this._missingValue = bind(this._missingValue, this);
  this._error = bind(this._error, this);
  this._watch = bind(this._watch, this);
  this.stop = bind(this.stop, this);
  this.stopped = false;
  this.retryAttempts = 0;
  this._watch();
}
```
- example usage
```shell
...

'''javascript
etcd.watch("key");
etcd.watch("key", console.log);
'''

The watch command is pretty low level, it does not handle reconnects or
timeouts (Etcd will disconnect you after 5 minutes). Use the '.watcher()' below
if you do not wish to handle this yourself.

### .watchIndex(key, index, [options], callback)

This is a convenience method for get with '{wait: true, waitIndex: index}'.

'''javascript
...
```

#### <a name="apidoc.element.node-etcd.watcher.EventEmitter"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.</span>EventEmitter ()](#apidoc.element.node-etcd.watcher.EventEmitter)
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

#### <a name="apidoc.element.node-etcd.watcher.init"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.</span>init ()](#apidoc.element.node-etcd.watcher.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-etcd.watcher.listenerCount"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.</span>listenerCount (emitter, type)](#apidoc.element.node-etcd.watcher.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-etcd.watcher.prototype"></a>[module node-etcd.watcher.prototype](#apidoc.module.node-etcd.watcher.prototype)

#### <a name="apidoc.element.node-etcd.watcher.prototype._error"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_error (err)](#apidoc.element.node-etcd.watcher.prototype._error)
- description and source-code
```javascript
_error = function (err) {
  var error;
  error = new Error('Connection error, reconnecting.');
  error.error = err;
  error.reconnectCount = this.retryAttempts;
  this.emit('reconnect', error);
  return this._retry();
}
```
- example usage
```shell
...
if (token.isAborted()) {
  return;
}
if (host == null) {
  if (this._shouldRetry(token)) {
    return this._retry(token, options, callback);
  }
  return this._error(token, callback);
}
reqRespHandler = (function(_this) {
  return function(err, resp, body) {
    if (token.isAborted()) {
      return;
    }
    if (_this._isHttpError(err, resp)) {
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._missingValue"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_missingValue (headers)](#apidoc.element.node-etcd.watcher.prototype._missingValue)
- description and source-code
```javascript
_missingValue = function (headers) {
  var error;
  error = new Error('Etcd timed out watcher, reconnecting.');
  error.headers = headers;
  this.retryAttempts = 0;
  this.emit('reconnect', error);
  return this._watch();
}
```
- example usage
```shell
...
    return;
  }
  if ((err != null ? err.errorCode : void 0) === 401 && (((ref = err.error) != null ? ref.index : void 0) != null)) {
    return this._resync(err);
  } else if (err) {
    return this._error(err);
  } else if (((headers != null ? headers['x-etcd-index'] : void 0) != null) && (val == null)) {
    return this._missingValue(headers);
  } else if ((val != null ? (ref1 = val.node) != null ? ref1.modifiedIndex : void 0 : void 0) != null) {
    return this._valueChanged(val, headers);
  } else {
    return this._unexpectedData(val, headers);
  }
};
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._respHandler"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_respHandler (err, val, headers)](#apidoc.element.node-etcd.watcher.prototype._respHandler)
- description and source-code
```javascript
_respHandler = function (err, val, headers) {
  var ref, ref1;
  if (this.stopped) {
    return;
  }
  if ((err != null ? err.errorCode : void 0) === 401 && (((ref = err.error) != null ? ref.index : void 0) != null)) {
    return this._resync(err);
  } else if (err) {
    return this._error(err);
  } else if (((headers != null ? headers['x-etcd-index'] : void 0) != null) && (val == null)) {
    return this._missingValue(headers);
  } else if ((val != null ? (ref1 = val.node) != null ? ref1.modifiedIndex : void 0 : void 0) != null) {
    return this._valueChanged(val, headers);
  } else {
    return this._unexpectedData(val, headers);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._resync"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_resync (err)](#apidoc.element.node-etcd.watcher.prototype._resync)
- description and source-code
```javascript
_resync = function (err) {
  this.index = err.error.index;
  this.retryAttempts = 0;
  this.emit('resync', err);
  return this._watch();
}
```
- example usage
```shell
...

  Watcher.prototype._respHandler = function(err, val, headers) {
var ref, ref1;
if (this.stopped) {
  return;
}
if ((err != null ? err.errorCode : void 0) === 401 && (((ref = err.error) != null ? ref.index : void 0) != null)) {
  return this._resync(err);
} else if (err) {
  return this._error(err);
} else if (((headers != null ? headers['x-etcd-index'] : void 0) != null) && (val == null)) {
  return this._missingValue(headers);
} else if ((val != null ? (ref1 = val.node) != null ? ref1.modifiedIndex : void 0 : void 0) != null) {
  return this._valueChanged(val, headers);
} else {
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._retry"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_retry ()](#apidoc.element.node-etcd.watcher.prototype._retry)
- description and source-code
```javascript
_retry = function () {
  var timeout;
  timeout = (Math.pow(2, this.retryAttempts) * 300) + (Math.round(Math.random() * 1000));
  setTimeout(this._watch, timeout);
  return this.retryAttempts++;
}
```
- example usage
```shell
...
host = _.first(servers);
options.url = "" + host + options.path;
if (token.isAborted()) {
  return;
}
if (host == null) {
  if (this._shouldRetry(token)) {
    return this._retry(token, options, callback);
  }
  return this._error(token, callback);
}
reqRespHandler = (function(_this) {
  return function(err, resp, body) {
    if (token.isAborted()) {
      return;
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._unexpectedData"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_unexpectedData (val, headers)](#apidoc.element.node-etcd.watcher.prototype._unexpectedData)
- description and source-code
```javascript
_unexpectedData = function (val, headers) {
  var error;
  error = new Error('Received unexpected response');
  error.response = val;
  this.emit('error', error);
  return this._retry();
}
```
- example usage
```shell
...
  } else if (err) {
    return this._error(err);
  } else if (((headers != null ? headers['x-etcd-index'] : void 0) != null) && (val == null)) {
    return this._missingValue(headers);
  } else if ((val != null ? (ref1 = val.node) != null ? ref1.modifiedIndex : void 0 : void 0) != null) {
    return this._valueChanged(val, headers);
  } else {
    return this._unexpectedData(val, headers);
  }
};

Watcher.prototype._retry = function() {
  var timeout;
  timeout = (Math.pow(2, this.retryAttempts) * 300) + (Math.round(Math.random() * 1000));
  setTimeout(this._watch, timeout);
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._valueChanged"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_valueChanged (val, headers)](#apidoc.element.node-etcd.watcher.prototype._valueChanged)
- description and source-code
```javascript
_valueChanged = function (val, headers) {
  this.retryAttempts = 0;
  this.index = val.node.modifiedIndex + 1;
  this.emit('change', val, headers);
  if (val.action != null) {
    this.emit(val.action, val, headers);
  }
  return this._watch();
}
```
- example usage
```shell
...
  if ((err != null ? err.errorCode : void 0) === 401 && (((ref = err.error) != null ? ref.index : void 0) != null)) {
    return this._resync(err);
  } else if (err) {
    return this._error(err);
  } else if (((headers != null ? headers['x-etcd-index'] : void 0) != null) && (val == null)) {
    return this._missingValue(headers);
  } else if ((val != null ? (ref1 = val.node) != null ? ref1.modifiedIndex : void 0 : void 0) != null) {
    return this._valueChanged(val, headers);
  } else {
    return this._unexpectedData(val, headers);
  }
};

Watcher.prototype._retry = function() {
  var timeout;
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype._watch"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>_watch ()](#apidoc.element.node-etcd.watcher.prototype._watch)
- description and source-code
```javascript
_watch = function () {
  if (this.index === null) {
    return this.request = this.etcd.watch(this.key, this.options, this._respHandler);
  } else {
    return this.request = this.etcd.watchIndex(this.key, this.index, this.options, this._respHandler);
  }
}
```
- example usage
```shell
...
  this._valueChanged = bind(this._valueChanged, this);
  this._missingValue = bind(this._missingValue, this);
  this._error = bind(this._error, this);
  this._watch = bind(this._watch, this);
  this.stop = bind(this.stop, this);
  this.stopped = false;
  this.retryAttempts = 0;
  this._watch();
}

Watcher.prototype.stop = function() {
  this.stopped = true;
  this.request.abort();
  return this.emit('stop', "Watcher for '" + this.key + "' aborted.");
};
...
```

#### <a name="apidoc.element.node-etcd.watcher.prototype.constructor"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>constructor (etcd, key, index, options)](#apidoc.element.node-etcd.watcher.prototype.constructor)
- description and source-code
```javascript
function Watcher(etcd, key, index, options) {
  this.etcd = etcd;
  this.key = key;
  this.index = index != null ? index : null;
  this.options = options != null ? options : {};
  this._retry = bind(this._retry, this);
  this._respHandler = bind(this._respHandler, this);
  this._resync = bind(this._resync, this);
  this._unexpectedData = bind(this._unexpectedData, this);
  this._valueChanged = bind(this._valueChanged, this);
  this._missingValue = bind(this._missingValue, this);
  this._error = bind(this._error, this);
  this._watch = bind(this._watch, this);
  this.stop = bind(this.stop, this);
  this.stopped = false;
  this.retryAttempts = 0;
  this._watch();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-etcd.watcher.prototype.stop"></a>[function <span class="apidocSignatureSpan">node-etcd.watcher.prototype.</span>stop ()](#apidoc.element.node-etcd.watcher.prototype.stop)
- description and source-code
```javascript
stop = function () {
  this.stopped = true;
  this.request.abort();
  return this.emit('stop', "Watcher for '" + this.key + "' aborted.");
}
```
- example usage
```shell
...
watcher.on("change", console.log); // Triggers on all changes
watcher.on("set", console.log);    // Triggers on specific changes (set ops)
watcher.on("delete", console.log); // Triggers on delete.
watcher2 = etcd.watcher("key", null, {recursive: true});
watcher2.on("error", console.log);
'''

You can cancel a watcher by calling '.stop()'.

Signals:
- 'change' - emitted on value change
- 'reconnect' - emitted on reconnect
- 'error' - emitted on invalid content
- '<etcd action>' - the etcd action that triggered the watcher (ex: set, delete).
- 'stop' - watcher was canceled.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
