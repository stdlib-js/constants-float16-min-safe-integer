<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Min Safe Integer

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Minimum safe [half-precision floating-point][half-precision-floating-point-format] integer.

<section class="installation">

## Installation

```bash
npm install @stdlib/constants-float16-min-safe-integer
```

</section>

<section class="usage">

## Usage

```javascript
var FLOAT16_MIN_SAFE_INTEGER = require( '@stdlib/constants-float16-min-safe-integer' );
```

#### FLOAT16_MIN_SAFE_INTEGER

The minimum [safe][safe-integers] [half-precision floating-point][half-precision-floating-point-format] integer.

```javascript
var bool = ( FLOAT16_MIN_SAFE_INTEGER === -2047 );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var pow = require( '@stdlib/math-base-special-pow' );
var FLOAT16_MIN_SAFE_INTEGER = require( '@stdlib/constants-float16-min-safe-integer' );

var min;
var x;
var i;

min = -pow( 2.0, 13 );
for ( i = 0; i < 100; i++ ) {
    x = round( randu() * min );
    if ( x < FLOAT16_MIN_SAFE_INTEGER ) {
        console.log( 'Unsafe: %d', x );
    } else {
        console.log( 'Safe: %d', x );
    }
}
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float16-min-safe-integer.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float16-min-safe-integer

[test-image]: https://github.com/stdlib-js/constants-float16-min-safe-integer/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/constants-float16-min-safe-integer/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float16-min-safe-integer/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float16-min-safe-integer?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float16-min-safe-integer
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float16-min-safe-integer/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float16-min-safe-integer/main/LICENSE

[safe-integers]: http://www.2ality.com/2013/10/safe-integers.html

[half-precision-floating-point-format]: https://en.wikipedia.org/wiki/Half-precision_floating-point_format

</section>

<!-- /.links -->
