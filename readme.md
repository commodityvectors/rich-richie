# RichJS [![Build Status](https://travis-ci.org/commodityvectors/rich-js.svg?branch=master)](https://travis-ci.org/commodityvectors/rich-js)

A JavaScript library for rich prototypes

This is a simple library designed to give a belt of good utility functions throughout your well known data types

## How to use

```javascript
var Rich = require('rich-js');
Rich.Core.applyAll(); // To apply all prototypes
Rich.Array.applyRichPrototype(); // Applies only the Array prototype
```

`npm install --save rich-js`  

## Safety

This library try not to clash with any possible standard when naming methods.

## Documentation

1. [Number](https://github.com/commodityvectors/rich-js/wiki/Number)
2. [Object](https://github.com/commodityvectors/rich-js/wiki/Object)
3. [Array](https://github.com/commodityvectors/rich-js/wiki/Array)

## Examples

A few examples of what this library offers

```javascript
//Number prototype
(3).minutes();
// 180000

(3).times(function(i) {
    console.log(i);
});
// 0
// 1
// 2

(3).isEven();
// false
(3).isOdd();
// true

// Object prototype
({
    prop: {
        name: 'Test'
    }
}).getProperty('prop.name');
// 'Test'

// Array prototype
[{a: 1}, {a: 1}, {a: 2}].groupBy('a');
/*
{
  1: [{a: 1}, {a: 1}],
  2: [{a: 2}]
}
*/
```
