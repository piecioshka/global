## There is one way to get global scope!

## On ECMAScript 3

```javascript
var global = (function(){return this})(); // ES3, ES5 disable strict mode
```

## On ECMAScript 5

```javascript
var global = (1,eval)('this'); // ES5 strict
```

## Cross-platform Solution

```javascript
"use strict";
var global = (function(){ return (1,eval)('this') })(); // ES3, ES5 with strict mode enable
```

or

```javascript
"use strict";
var global = new Function("return this")();
```

## Try to read, and don't cry!

* http://perfectionkills.com/unnecessarily-comprehensive-look-into-a-rather-insignificant-issue-of-global-objects-creation/#ecmascript_5_strict_mode
* http://perfectionkills.com/global-eval-what-are-the-options/
