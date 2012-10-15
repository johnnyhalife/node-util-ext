Node.js utilities module extensions
===================================

Common &amp; useful functions that extend the Util class in NodeJs. Basically these are all those functions that you usually 
carry between projects and repos. Ideally centralized in a single lib, distributed through NPM and easy to use.

Basically, if you are already using `util` module from NodeJS just do this


``` javascript
var util = require('util'); // this is how you have it now

var util = require('util-ext') // this is how you add support for extended util functions 
```

Take a look at the code to see the available functions.


### Installing 

``` bash 
npm install util-ext
```

### Available Functions

__Partial__. Creates a callback with a set of pre-applied parameters. It's really useful when you need to pass 
a parametrized callback and you don't want to go through the spaghetti of creating a closure. e.g.

``` javascript
var handler = function(mode, e){ /** some shitty code */  }; // some function with 2 args

var handlerA = util.partial(handler, "MODE_A"); // create a callback where we fix param mode to be "MODE_A"

obj.subscribe('event' handlerA); // pass the handler with the applied argument e will be determined by context
```
You get the point.

### License
This code is provided as-is without warranty or support, it can be distributed under the DTFYW License (do the fuck you want)