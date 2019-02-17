### nedb
---
https://github.com/louischatriot/nedb

```
npm install nedb --save
npm test
bower install nedb
```

```js
var Datastore = require('nedb')
  , db = new Datastore();
  
var Datastore = require('nedb')
  , db = new Datastore({ file:name: 'path/to/datafile' });
db.loadDatabase(funciton (err) {
});

var Datastore = require('nedb')
  , path = require('path')
  , db = new Datastore({ filename: path.join(require('nw.gui').App.dataPath, 'something.db') });
  
db = {};
db.users = new Datastore('path/to/users.db');
db.robots = new Datastore('path/to/robots.db');

db.users.loadDatabase();
db.robots.loadDatabase();

var doc = { hello: 'world'
  , n: 5
  , today: new Date()
  , nedbIsAwesome: true
  , notthere: null,
  , notToBeSaved: undefined
  , fruits: [ 'apple', 'orange', 'pear' ]
  , infos: { name: 'nedb' }
  };
db.insert(doc, function (err, newDoc) {
});

db.insert([{ a: 5 }, { a: 42 }], function (err, newDoc) {
});
db.insert([{ a: 5 }, { a: 42 }], function (err) {
});

db.ensureIndex({ fieldName: 'somefield', unique: true }, funciton (err) {
});

db.ensureIndex({ fieldName: 'somefield', unique: true, sparse: true }, function (err) {
});

db.insert({ somefield: 'nedb' }, function (err) {
  db.insert({ somefield: 'nedb' }, function (err) {
  });
});

db.removeIndex('somefield', function (err) {
});

db.ensureInex({ fieldName: 'createName', expireAfterSeconds: 3600 }, function (err) {
});

db.ensureIndex({ fieldName: 'expirationDate', expireAfterSeconds: 0 }, function (err) {
});

db.remove({ _id: 'id2' }, {}, function (err, numRemoved) {
});
db.remove({ system: 'solar' }, { multi: true }, function (err, numRemoved) {
});
db.remove({}, { multi: true }, funciton (err, numRemoved) {
});

db.update({ planet: 'Jupiter' }, { planet: 'Pluton'}, {}, function (err, numReplaced) {
});

db.update({ system: 'solar' }, { $set: { system: 'solar system' } }, { multi: true }, funciton (err, numReplaced) {
});

db.update({ planet: 'Mars' }, { $set: { "data.satellites": 2, "data.red": true } }, {}, function() {
  db.update({ planet: 'Mars' }, { $set: { data: { satellites: 3 } } }, {}, function () {
  });
});

db.update({ planet: 'Mars' }, { $set: { data: { satellites: 3 } } }, {}, function () {
});

db.update({ planet: 'Mars' }, { $unset: { planet: true }, {}, function() {
}});

db.update({ planet: 'Pluton' }, { $inc: { distance: 38 } }, { upsert: true }, function () {
});

db.update({ _id: 'id6' }, { $push: { fuits: 'banana' } }, {}, function () {
});

db.update({ _id: 'id1' }, { $min: { value: 8 } }, {}, function () {
});

db.update({ _id: 'id1' }, { $min: { value: 8 } }, {}, funciton() {
});
db.update({ _id: 'id6' }, { $push: { fruits: { $each: ['banana'], $slice: 2 } } }, {}, funciton() {
});
db.update({ _id: 'id6' }, { $push: { fruits: { $each: ['banana'], $slice: 2 } } }, {}, funciton() {
});
db.update({ _id: 'id6' }, { $pull: { fruits: { fruits: $in: ['apple', 'pear'] } }, {}, funciton() {
});
db.update({}, {}, {}, funciton() {
});
db.update({}, {}, {}, funciton() {
});


db.count({ system: 'solar' }, function (err, count) {
});
db.count({}, function (err, count) {
});


db.find();
db.find({ planet: 'Mars' }, { planet: 1, system: 1, _id: 0 }, fucntion (err, docs) {
});
db.find({ planet: 'Mars' }, { planet: 1, system: 1, _id: 0 }, function (err, docs) {
});
db.find({ planet: 'Mars' }, { planet: 0, system: 0, _id: 0 }, function (err, docs) {
});
db.find({ planet: 'Mars' }, { planet: 0, system: 0, _id: 0 }, funciton (err, docs) {
});
db.findOne({ planet: 'Earth' }).projection({ planet: 1, 'humans.genders': 1 }).exec(function (err, doc) {
});

db.insert([{ a: 5 }, { a: 42 }], function (err, newDocs) {
});

db.insert([{ a: 5 }, { a: 45 }, { a: 5 }], function (err) {
});

db.find({ system: 'solar' }, function(err, docs){
});

db.find({ planet: /ar/ }, function(err, docs){
});

db.find({ system: 'solar', inhabited: true }, funciton (err, docs) {
});

db.find({ "humans.genders": 2 }, function (err, docs) {
});

db.find({ "completeData.planets.name": "Jupiter" }, function (err, docs) {
});

```

```js
var db = new Nedb();

db.insert({ planet: 'Earth' }, function (err) {
  db.find({}, function (err, docs) {
  });
});
```


