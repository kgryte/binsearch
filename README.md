Binsearch
=========

Perform a 1d bin search where bins are defined by an input edge vector.


## Examples

``` javascript
var binsearch = require( 'binsearch' ),
	edges, numEdges = 11,
	idx;

// Create a 1d edge array...
edges = new Array( numEdges );

// Note: numBins = numEdges-1
for ( var i = 0; i < numEdges; i++ ) {
	edges[ i ] = i-0.5;
}

// Perform a bin search...
idx = binsearch( edges, 0 );
// returns idx = 0

idx = binsearch( edges, 1 );
// returns idx = 1

idx = binsearch( edges, 5.2345 );
// returns idx = 5

idx = binsearch( edges, 5.5001 );
// returns idx = 6

idx = binsearch( edges, -5 );
// returns idx = -1

idx = binsearch( edges, 100 );
// returns idx = 10
```

## Tests

Unit tests use the [Mocha](http://visionmedia.github.io/mocha) test framework with [Chai](http://chaijs.com) assertions.

Assuming you have installed Mocha, execute the following command in the top-level application directory to run the tests:

``` bash
$ mocha
```

All new feature development should have corresponding unit tests to validate correct functionality.


## License

[MIT license](http://opensource.org/licenses/MIT). 


---
## Copyright

Copyright &copy; 2014. Athan Reines.

