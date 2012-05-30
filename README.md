## It's one way to get global scope.

## On ECMAScript 3
var global = (function(){return this})(); // ES3, ES5 non strict

## On ECMAScript 5
var global = (1,eval)('this'); // ES5 strict

## Cross-platform Solution
var global = (function(){ return this || (1,eval)('this') })();

## Try to read, and don't cry!
http://perfectionkills.com/unnecessarily-comprehensive-look-into-a-rather-insignificant-issue-of-global-objects-creation/#ecmascript_5_strict_mode