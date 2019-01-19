### director
---
https://github.com/flatiron/director

```js
var director = require('director');
var router = new director.http.Router();
router.get('/', { stream: true }, function(){
  this.req.on('data', function(chunk){
    console.log(chunk);
  });
});

var http = require('http');
  director = require('director');
var router = new director.http.Router();
var server = http.createServer(function(req, res){
  req.chunks = [];
  req.on('data', function(chunk){
    req.chunks.push(chunk.toString());
  });
  router.dispatch(req, res, function(err){
    if(err){
      res.writeHead(404);
      res.end();
    }
    console.log('Served' + req.url);
  });
});
router.post('/', function(){
  this.res.writeHead(200, { 'Cotent-Type': 'application/json' })
  this.res.end(JSON.stringify(this.req.body));
});

var director = require('director');
var router = new director.http.Router();
router.get('/', function(){
  this.req.on('data', function(chunk){
    console.log(chunk)
  });
});

var director = require('director');
var router = new director.http.Router().configure(options);
router.attach(function(){
  this.data = [1,2,3];
});
router.get('/hello', function(){
  this.res.writeHead(200, { 'content-type': 'text/plain' });
  this.res.end(this.data);
});

var router = Router({
  '/hello': {
    '/usa': 'americas',
    '/china': 'asia'
  }
}).configure({ resource: container }).init();
var container = {
  americas: function(){ return true; },
  china: function(){ return true; }
};

var router = new director.Router();
router.on('/:foo/:bar/:bazz', function(foo, bar, bazz){
});

var router = new director.http.Router().configure({ async: true });
router.on('/:foo/:bar/:bazz', function(foo, bar, bazz, next){
  next(false);
});

var routes = {
  '/dog': {
    '/angry': {
      on: function(){ return false; }
    },
    on: bark
  },
};
var router = Router(routes).configure({ recure: 'backward' });

var routes = {
  '/dog': {
    '/angry': {
      on: growl
    },
    on: bark
  }
};

var routes = {
  '/dog': {
    '/angry': {
      on: growl
    },
    on: bark
  }
};
var router = Router(routes);
  
var routes = {
  '/dog': {
    '/angry': {
      on: growl
    },
    on: bark
  }
};
var router = Router(routes).configure({ recurse: 'backward' });

router.on("/foo/>((\w|.)*)"), function(path){};

var router = new director.Router();
router.on(/([\w-_]+)/, function(userId){ });
router.param('userId', /([\\w\\-]+)/);
router.on('/anything/:userId', function(userId){ });
router.on('/something-else/:userId', function(userId){ });

var router = Router({
  '/hello': {
    '/world/?([^\/]*)\/([^\/]*)/?': function(a,b){
      console.log(a, b);
    }
  }
});

var router = Router({
  '/hello': {
    '/(\\w+)': {
     on: function(who){ console.log(who) }
    }
  }
});

var router = Router({
  '/hello': {
    '/(\\w+)': {
      on: function(who){ console.log(who) }
    }
  }
});

var router = Router({
  '/dog': {
    '/:color': {
      on: function(color){ console.log(color) }
    }
  }
});

var router = new director.Router(router).configure(options);

var router = new director.http.Router();
router.path(/\/users\/(\w+)/, function(){
  this.post(function(id){
  });
  this.get(function(id){
  });
  this.get(/\/friends/, function(id){
  });
});

var router = new director.http.Router();
router.get(/\/some\/resource/, function(){
});

var router = new Router().init();
router.on('/some/resource', function(){
});

var routes = {
  '/dog': bark,
  '/cat': [meow, scratch]
};
var router = Router(routes);

var router = Router(routes);
```

```
```

```
```

