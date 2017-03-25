# api documentation for  [gulp-html-replace (v1.6.2)](https://github.com/VFK/gulp-html-replace#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-html-replace.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-html-replace)
#### Replace build blocks in HTML. Like useref but done right.

[![NPM](https://nodei.co/npm/gulp-html-replace.png?downloads=true)](https://www.npmjs.com/package/gulp-html-replace)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-gulp_html_replace_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-gulp-html-replace/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Vladimir Kucherenko",
        "email": "kvsoftware@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/VFK/gulp-html-replace/issues"
    },
    "contributors": [
        {
            "name": "Bruce MacNaughton",
            "email": "bmacnaughton@gmail.com"
        }
    ],
    "dependencies": {
        "bluebird": "^3.1.1",
        "clone": "^1.0.2",
        "object-assign": "^4.0.1",
        "readable-stream": "^2.0.4",
        "slash": "^1.0.0",
        "vinyl-buffer": "^1.0.0"
    },
    "description": "Replace build blocks in HTML. Like useref but done right.",
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
    "directories": {},
    "dist": {
        "shasum": "1e1066fa6f8538c8d199e99a3443472f2bb46242",
        "tarball": "https://registry.npmjs.org/gulp-html-replace/-/gulp-html-replace-1.6.2.tgz"
    },
    "engines": {
        "node": ">= 0.9"
    },
    "files": [
        "lib"
    ],
    "gitHead": "4b99045040b3fbf79a2702a64276ec78a2e2b771",
    "homepage": "https://github.com/VFK/gulp-html-replace#readme",
    "keywords": [
        "gulpplugin",
        "html",
        "replace"
    ],
    "license": "MIT",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "vfk",
            "email": "kvsoftware@gmail.com"
        }
    ],
    "name": "gulp-html-replace",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/VFK/gulp-html-replace.git"
    },
    "scripts": {
        "coverage": "istanbul cover _mocha -- -R dot",
        "coveralls": "istanbul cover _mocha && istanbul-coveralls",
        "test": "mocha"
    },
    "version": "1.6.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module gulp-html-replace](#apidoc.module.gulp-html-replace)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.</span>block (config, file, match)](#apidoc.element.gulp-html-replace.block)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.</span>parser (tasks, config, file)](#apidoc.element.gulp-html-replace.parser)
1.  object <span class="apidocSignatureSpan">gulp-html-replace.</span>block.prototype
1.  object <span class="apidocSignatureSpan">gulp-html-replace.</span>common
1.  object <span class="apidocSignatureSpan">gulp-html-replace.</span>parser.prototype

#### [module gulp-html-replace.block](#apidoc.module.gulp-html-replace.block)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.</span>block (config, file, match)](#apidoc.element.gulp-html-replace.block.block)

#### [module gulp-html-replace.block.prototype](#apidoc.module.gulp-html-replace.block.prototype)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.block.prototype.</span>build ()](#apidoc.element.gulp-html-replace.block.prototype.build)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.block.prototype.</span>compile (tasks)](#apidoc.element.gulp-html-replace.block.prototype.compile)

#### [module gulp-html-replace.common](#apidoc.module.gulp-html-replace.common)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.common.</span>parseTasks (options)](#apidoc.element.gulp-html-replace.common.parseTasks)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.common.</span>regexMatchAll (string, regexp)](#apidoc.element.gulp-html-replace.common.regexMatchAll)

#### [module gulp-html-replace.parser](#apidoc.module.gulp-html-replace.parser)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.</span>parser (tasks, config, file)](#apidoc.element.gulp-html-replace.parser.parser)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.parser.</span>super_ (options)](#apidoc.element.gulp-html-replace.parser.super_)

#### [module gulp-html-replace.parser.prototype](#apidoc.module.gulp-html-replace.parser.prototype)
1.  [function <span class="apidocSignatureSpan">gulp-html-replace.parser.prototype.</span>_transform (chunk, enc, done)](#apidoc.element.gulp-html-replace.parser.prototype._transform)



# <a name="apidoc.module.gulp-html-replace"></a>[module gulp-html-replace](#apidoc.module.gulp-html-replace)

#### <a name="apidoc.element.gulp-html-replace.block"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.</span>block (config, file, match)](#apidoc.element.gulp-html-replace.block)
- description and source-code
```javascript
block = function (config, file, match) {
    this.replacement = match[0];
    this.linefeed = match[1];
    this.indent = match[2];
    this.beginTag = match[3];
    this.taskName = match[4];
    this.originalContent = match[5];
    this.endTag = match[6];

    this.replacements = [];
    this.config = config;
    this.template = null;
    this.file = file;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-html-replace.parser"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.</span>parser (tasks, config, file)](#apidoc.element.gulp-html-replace.parser)
- description and source-code
```javascript
function Parser(tasks, config, file) {
    Transform.call(this);

    this.tasks = tasks;
    this.config = config;
    this.file = file;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.gulp-html-replace.block"></a>[module gulp-html-replace.block](#apidoc.module.gulp-html-replace.block)

#### <a name="apidoc.element.gulp-html-replace.block.block"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.</span>block (config, file, match)](#apidoc.element.gulp-html-replace.block.block)
- description and source-code
```javascript
block = function (config, file, match) {
    this.replacement = match[0];
    this.linefeed = match[1];
    this.indent = match[2];
    this.beginTag = match[3];
    this.taskName = match[4];
    this.originalContent = match[5];
    this.endTag = match[6];

    this.replacements = [];
    this.config = config;
    this.template = null;
    this.file = file;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.gulp-html-replace.block.prototype"></a>[module gulp-html-replace.block.prototype](#apidoc.module.gulp-html-replace.block.prototype)

#### <a name="apidoc.element.gulp-html-replace.block.prototype.build"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.block.prototype.</span>build ()](#apidoc.element.gulp-html-replace.block.prototype.build)
- description and source-code
```javascript
build = function () {
    if (!this.replacements.length) {
        return this.config.keepUnassigned ? [this.indent + this.originalContent.trim()] : [];
    }

    // get the replacement strings and do replacements for extensions
    if (this.uniqueExts) {
        var extname = path.extname(this.file.path);
        var basename = path.basename(this.file.path, extname);

        if (this.uniqueExts['%f']) {
            this.uniqueExts['%f'].value = basename;
        }
        if (this.uniqueExts['%e']) {
            this.uniqueExts['%e'].value = extname;
        }

        Object.keys(this.uniqueExts).forEach(function (key) {
            var unique = this.uniqueExts[key];
            this.template = this.template.replace(unique.regex, unique.value);
        }.bind(this));
    }

    if (this.srcIsNull) {
        return [this.indent + this.template];
    }

    return this.replacements.map(function (replacement) {
        if (this.template) {
            if (Array.isArray(replacement)) {
                replacement.unshift(this.template);
                return this.indent + util.format.apply(util, replacement);
            } else {
                return this.indent + util.format(this.template, replacement);
            }
        }

        if (this.config.resolvePaths) {
            var replacementPath = path.resolve(this.file.cwd, replacement);
            replacement = path.relative(path.dirname(this.file.path), replacementPath);
            replacement = slash(replacement);
        }

        var ext = replacement.split('?')[0].toLowerCase().split('.').pop();

        if (ext === 'js') {
            return util.format('%s<script src="%s"></script>', this.indent, replacement);
        } else if (ext === 'css') {
            return util.format('%s<link rel="stylesheet" href="%s">', this.indent, replacement);
        }
        return this.indent + replacement;
    }.bind(this));
}
```
- example usage
```shell
...
if (task) {
    this.replacements = task.src;
    this.template = task.tpl;
    this.uniqueExts = task.uni;
    this.srcIsNull = task.srcIsNull;
}

var buildResult = this.build();

if (this.config.keepBlockTags) {
    buildResult.unshift(this.indent + this.beginTag);
    buildResult.push(this.indent + this.endTag);
}

buildResult.unshift(null);
...
```

#### <a name="apidoc.element.gulp-html-replace.block.prototype.compile"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.block.prototype.</span>compile (tasks)](#apidoc.element.gulp-html-replace.block.prototype.compile)
- description and source-code
```javascript
compile = function (tasks) {
    var task = tasks[this.taskName];

    if (task) {
        this.replacements = task.src;
        this.template = task.tpl;
        this.uniqueExts = task.uni;
        this.srcIsNull = task.srcIsNull;
    }

    var buildResult = this.build();

    if (this.config.keepBlockTags) {
        buildResult.unshift(this.indent + this.beginTag);
        buildResult.push(this.indent + this.endTag);
    }

    buildResult.unshift(null);
    buildResult.push(null);

    return buildResult.join(this.linefeed);
}
```
- example usage
```shell
...
Parser.prototype._transform = function (chunk, enc, done) {
    var content = chunk.toString('utf8');

    var matches = common.regexMatchAll(content, regex);
    matches.forEach(function (match) {
        var block = new Block(this.config, this.file, match);
        content = content.replace(block.replacement, function () {
            return block.compile(this.tasks)
        }.bind(this));
    }.bind(this));

    done(null, content);
};

module.exports = Parser;
...
```



# <a name="apidoc.module.gulp-html-replace.common"></a>[module gulp-html-replace.common](#apidoc.module.gulp-html-replace.common)

#### <a name="apidoc.element.gulp-html-replace.common.parseTasks"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.common.</span>parseTasks (options)](#apidoc.element.gulp-html-replace.common.parseTasks)
- description and source-code
```javascript
parseTasks = function (options) {
    options = options || {};

    var utilExtensions = /%f|%e/g;
    var tasksByNames = {};

    var tasksPromises = Object.keys(options).map(function (name) {

        var task = {
            src: [],
            tpl: null,
            uni: {},
            srcIsNull: false
        };

        return Promise
            .resolve()
            .then(function () {
                var item = options[name];
                var src = typeof item.src !== 'undefined' ? item.src : item;

                return resolveSrcString(src)
                  .then(function(srcStrings) {
                      task.srcIsNull = srcStrings === null;
                      task.src = task.src.concat(srcStrings);
                      task.tpl = item.tpl;
                  });
            })
            .then(function () {
                var result;

                while (result = utilExtensions.exec(task.tpl)) {
                    var type = result[0];
                    var unique = {};

                    if (task.uni[type]) {
                        continue;
                    }

                    unique.regex = new RegExp(result[0], "g");
                    unique.value = null;
                    task.uni[type] = unique;
                }
            })
            .then(function () {
                tasksByNames[name] = task;
            });
    });

    return Promise.all(tasksPromises)
        .then(function() {
           return tasksByNames;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-html-replace.common.regexMatchAll"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.common.</span>regexMatchAll (string, regexp)](#apidoc.element.gulp-html-replace.common.regexMatchAll)
- description and source-code
```javascript
regexMatchAll = function (string, regexp) {
    var matches = [];
    string.replace(regexp, function () {
        var arr = Array.prototype.slice.call(arguments);
        matches.push(arr);
    });
    return matches;
}
```
- example usage
```shell
...
this.file = file;
}
util.inherits(Parser, Transform);

Parser.prototype._transform = function (chunk, enc, done) {
var content = chunk.toString('utf8');

var matches = common.regexMatchAll(content, regex);
matches.forEach(function (match) {
    var block = new Block(this.config, this.file, match);
    content = content.replace(block.replacement, function () {
        return block.compile(this.tasks)
    }.bind(this));
}.bind(this));
...
```



# <a name="apidoc.module.gulp-html-replace.parser"></a>[module gulp-html-replace.parser](#apidoc.module.gulp-html-replace.parser)

#### <a name="apidoc.element.gulp-html-replace.parser.parser"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.</span>parser (tasks, config, file)](#apidoc.element.gulp-html-replace.parser.parser)
- description and source-code
```javascript
function Parser(tasks, config, file) {
    Transform.call(this);

    this.tasks = tasks;
    this.config = config;
    this.file = file;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-html-replace.parser.super_"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.parser.</span>super_ (options)](#apidoc.element.gulp-html-replace.parser.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.gulp-html-replace.parser.prototype"></a>[module gulp-html-replace.parser.prototype](#apidoc.module.gulp-html-replace.parser.prototype)

#### <a name="apidoc.element.gulp-html-replace.parser.prototype._transform"></a>[function <span class="apidocSignatureSpan">gulp-html-replace.parser.prototype.</span>_transform (chunk, enc, done)](#apidoc.element.gulp-html-replace.parser.prototype._transform)
- description and source-code
```javascript
_transform = function (chunk, enc, done) {
    var content = chunk.toString('utf8');

    var matches = common.regexMatchAll(content, regex);
    matches.forEach(function (match) {
        var block = new Block(this.config, this.file, match);
        content = content.replace(block.replacement, function () {
            return block.compile(this.tasks)
        }.bind(this));
    }.bind(this));

    done(null, content);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
