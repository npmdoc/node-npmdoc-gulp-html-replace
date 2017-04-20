# npmdoc-gulp-html-replace

#### api documentation for  gulp-html-replace (v1.6.2)  [![npm package](https://img.shields.io/npm/v/npmdoc-gulp-html-replace.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-gulp-html-replace) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-html-replace.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-html-replace)

#### Replace build blocks in HTML. Like useref but done right.

[![NPM](https://nodei.co/npm/gulp-html-replace.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/gulp-html-replace)

- [https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "gulp-html-replace",
    "version": "1.6.2",
    "description": "Replace build blocks in HTML. Like useref but done right.",
    "keywords": [
        "gulpplugin",
        "html",
        "replace"
    ],
    "files": [
        "lib"
    ],
    "repository": {
        "type": "git",
        "url": "https://github.com/VFK/gulp-html-replace.git"
    },
    "author": {
        "name": "Vladimir Kucherenko"
    },
    "contributors": [
        {
            "name": "Bruce MacNaughton"
        }
    ],
    "main": "./lib/index.js",
    "scripts": {
        "test": "mocha",
        "coverage": "istanbul cover _mocha -- -R dot",
        "coveralls": "istanbul cover _mocha && istanbul-coveralls"
    },
    "engines": {
        "node": ">= 0.9"
    },
    "dependencies": {
        "bluebird": "^3.1.1",
        "clone": "^1.0.2",
        "object-assign": "^4.0.1",
        "readable-stream": "^2.0.4",
        "slash": "^1.0.0",
        "vinyl-buffer": "^1.0.0"
    },
    "devDependencies": {
        "concat-stream": "^1.5.1",
        "from2-string": "^1.1.0",
        "gulp-util": "^3.0.7",
        "istanbul": "^0.4.0",
        "istanbul-coveralls": "^1.0.3",
        "mocha": "^2.3.4",
        "vinyl": "^1.1.0",
        "vinyl-source-stream": "^1.1.0"
    },
    "license": "MIT"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
