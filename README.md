# npmdoc-node-etcd

#### api documentation for  [node-etcd (v5.0.3)](https://github.com/stianeikeland/node-etcd#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-etcd.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-etcd) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-etcd.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-etcd)

#### etcd library for node.js (etcd v2 api)

[![NPM](https://nodei.co/npm/node-etcd.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/node-etcd)

- [https://npmdoc.github.io/node-npmdoc-node-etcd/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-node-etcd/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-etcd/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-etcd/build/apidoc.html)

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
            "name": "stiane"
        }
    ],
    "name": "node-etcd",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
