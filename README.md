<<<<<<< HEAD
# mongo

The `mongo` package is a [full stack database
driver](https://www.meteor.com/full-stack-db-drivers) that provides
several paramount pieces of functionality to work with MongoDB in
Meteor:

- an efficient [Livequery][livequery] implementation providing real-time
  updates from the database by consuming the MongoDB replication log
- a fall-back Livequery implementation for cases when the replication log is not
  available, implemented by polling the database
- DDP RPC end-points for updating the data from clients connected over the wire
- Serialization and deserialization of updates to the DDP format

To learn more about Livequery, see the [project page on
www.meteor.com][livequery].

[livequery]: https://www.meteor.com/livequery

## Direct access to npm mongodb API

On the server, the `mongo` package is implemented using the
[npm `mongodb` module](https://www.npmjs.com/package/mongodb).  If you'd like
direct access to this module, you can find it at
`MongoInternals.NpmModules.mongodb.module`. Its version can be read at
`MongoInternals.NpmModules.mongodb.version`.

Additionally, you can call `c.rawCollection()` or `c.rawDatabase()` on any
`Mongo.Collection` to get the object from the npm `mongodb` module corresponding
to the collection or database.  This is documented at
http://mongodb.github.io/node-mongodb-native/

The version of `mongo` used may change incompatibly from version to version of
Meteor (or we may even replace it with an entirely different implementation);
use at your own risk.
=======

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
>>>>>>> e3d6674... Make compatible with React Native and NodeJS
