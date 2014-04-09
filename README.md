# read-data [![NPM version](https://badge.fury.io/js/read-data.png)](http://badge.fury.io/js/read-data)

> Utils for reading JSON and YAML data files.

## Install
Install with [npm](npmjs.org):

```bash
npm i read-data --save
```


## api
### JSON

#### readJSON

Read JSON files asynchronously.

```js
var file = require('read-data');
file.readJSON('foo.json', callback);
```

#### readJSONSync

Read JSON files synchronously.

```js
var file = require('read-data');
file.readJSONSync('foo.json');
```


### YAML

#### readYAML

Read YAML files asynchronously.

```js
var file = require('read-data');
file.readYAML('foo.yaml', callback);
```

#### readYAMLSync

Read YAML files synchronously.

```js
var file = require('read-data');
file.readYAMLSync('foo.yaml');
```


### Data (automatic)

Automatically read a JSON or YAML data file based on its file extension.

#### readData

Read JSON or YAML files asynchronously.

```js
var file = require('read-data');
file.readData('foo.json', callback);
file.readData('foo.yml', callback);
```

#### readDataSync

Read JSON or YAML files synchronously.

```js
var file = require('read-data');
file.readDataSync('foo.json');
file.readDataSync('foo.yml');
```

#### lang

With the `readData` methods, you can also explicitly set the language to read by passing a `lang` option as a second parameter.

```js
file.readDataSync('foo.json', {lang: 'json'});
```

This is useful if you need to set this value dynamically.

## Authors

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

**Brian Woodward**

+ [github/doowb](https://github.com/doowb)
+ [twitter/doowb](http://twitter.com/jonschlinkert)

## License
Copyright (c) 2014 Jon Schlinkert, contributors.  
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on April 09, 2014._