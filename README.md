## There is one way to get global scope!

## On ECMAScript 3
```
var global = (function(){return this})(); // ES3, ES5 disable strict mode
```

## On ECMAScript 5
```
var global = (1,eval)('this'); // ES5 strict
```

## Cross-platform Solution
```
"use strict";
var global = (function(){ return (1,eval)('this') })(); // ES3, ES5 with strict mode enable
```

## Try to read, and don't cry!

http://perfectionkills.com/unnecessarily-comprehensive-look-into-a-rather-insignificant-issue-of-global-objects-creation/#ecmascript_5_strict_mode

http://perfectionkills.com/global-eval-what-are-the-options/
