# read-data [![NPM version](https://badge.fury.io/js/read-data.svg)](http://badge.fury.io/js/read-data)  [![Build Status](https://travis-ci.org/jonschlinkert/read-data.svg)](https://travis-ci.org/jonschlinkert/read-data) 

> Utils for reading JSON and YAML data files.

## Install with [npm](npmjs.org)

```bash
npm i read-data --save
```

## API
### [.readJSON](./index.js#L35)

Read JSON file asynchronously and parse content as JSON

* `filepath` **{String}**: path of the file to read.    
* `callback` **{Function}**: callback function    
* `returns` **{Object}**: JSON  

**Example:**

```js
var file = require('read-data');

file.readJSON('config.json', function(err, data) {
  if (err) throw err;
  console.log(data);
});
```

### [.readJSONSync](./index.js#L69)

Read JSON file synchronously and parse content as JSON

* `filepath` **{String}**: path of the file to read.    
* `returns` **{Object}**: JSON  

**Example:**

```js
var file = require('read-data');

var config = file.readJSONSync('config.json');
```

### [.readYAML](./index.js#L99)

Read YAML file asynchronously and parse content as JSON

* `filepath` **{String}**: path of the file to read.    
* `options` **{Object|String}**: to pass to [js-yaml]    
* `cb` **{Function}**: callback function    
* `returns` **{Object}**: JSON  

**Example:**

```js
var file = require('read-data');

file.readYAML('config.yml', function(err, data) {
  if (err) throw err;
  console.log(data);
});
```

### [.readYAMLSync](./index.js#L119)

Read YAML file synchronously and parse content as JSON

* `filepath` **{String}**: path of the file to read.    
* `options` **{Object|String}**: to pass to [js-yaml]    
* `returns` **{Object}**: JSON  

**Example:**

```js
var file = require('read-data');

var config = file.readYAMLSync('config.yml');
var config = file.readYAML.sync('config.yml');
var config = file.readYaml.sync('config.yml');
```

### [.readData](./index.js#L147)

Determine the reader based on extension, asynchronously

* `filepath` **{String}**: path of the file to read.    
* `options` **{Object|String}**: to pass to [js-yaml]    
* `cb` **{Function}**: callback function    
* `returns` **{Object}**: JSON  

**Example:**

```js
var file = require('read-data');

file.readData('config.json', function(err, data) {
  if (err) throw err;
  console.log(data);
});

file.readData('config.yml', function(err, data) {
  if (err) throw err;
  console.log(data);
});
```

### [.readDataSync](./index.js#L184)

Determine the reader based on extension, synchronously

* `filepath` **{String}**: path of the file to read.    
* `options` **{Object|String}**: to pass to [js-yaml]    
* `returns` **{Object}**: JSON  

**Example:**

```js
var file = require('read-data');

var configYAML = file.readDataSync('config.yml');
var configJSON = file.readDataSync('config.json');
```

### [.readOptionalJSON](./index.js#L207)

* `filepath` **{String}**: path of the file to read.    
* `returns` **{Object}**: JSON  

[Read optional](https://gist.github.com/2876125) JSON by Ben Alman

### [.readOptionalYAML](./index.js#L223)

* `filepath` **{String}**: path of the file to read.    
* `options` **{Object|String}**: to pass to [js-yaml]    
* `returns` **{Object}**: JSON  

[Read optional](https://gist.github.com/2876125) YAML by Ben Alman

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2014-2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on March 31, 2015._

[js-yaml]: https://github.com/nodeca/js-yaml
