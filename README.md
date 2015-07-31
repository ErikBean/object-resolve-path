# object-resolve-path
a simple utility function for getting a value at a path from an object with all the usecases properly covered

## Install
```
npm i object-resolve-path
```

## Usage

```javascript
var resolvePath = require('object-resolve-path');
resolvePath(someObject, 'a.b[0]');	//returns first property from b from a from someObject
```

## Typical usecase?
Most other libraries for accessing deeply nested properties of an object don't work with bracket syntax. This one does work with bracket syntax. Just don't put bracket pairs into your keys like [here](https://github.com/capaj/object-resolve-path/blob/1.0.0/test/object-resolve-path.spec.js#L8). It will convert them into a '.' notation and fail.

For thorough description, check the [tests](https://github.com/capaj/object-resolve-path/blob/master/test/object-resolve-path.spec.js).

### Similar modules:

https://github.com/deoxxa/dotty (works only for dots)

https://github.com/Ntran013/dot-access  (works only for dots)

https://github.com/substack/js-traverse (much more complex and useful)
