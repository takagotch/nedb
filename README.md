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











```

```
```


