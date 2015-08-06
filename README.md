
# mongo v1.1.1 [![experimental](http://badges.github.io/stability-badges/dist/experimental.svg)](http://github.com/badges/stability-badges)

This package is stripped from [meteor/mongo](https://atmospherejs.com/meteor/mongo) and made compatible with [React Native](https://github.com/facebook/react-native).

**Note:** This package is only for client-side usage.

&nbsp;

## usage

```js
var Mongo = require('mongo');
var Meteor = require('meteor-client');

var collection = new Mongo.Collection('users', {
  connection: Meteor.connection,        // The DDP connection to use (defaults to Meteor.connection)
  autoPublish: false,                   // Used in place of "meteor/autopublish"
  insecure: false,                      // Used in place of "meteor/insecure"
  idGeneration: 'MONGO',                // The method of generating the `_id` fields of new documents in this collection (defaults to 'STRING')
  transform: function () { /* ... */ }, // Function that is passed the results of `fetch()` or `findOne()`
});
```

&nbsp;

## install

```sh
npm install aleclarson/mongo#1.1.1
```
