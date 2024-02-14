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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Min Safe Integer

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Minimum safe [half-precision floating-point][half-precision-floating-point-format] integer.



<section class="usage">

## Usage

```javascript
import FLOAT16_MIN_SAFE_INTEGER from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float16-min-safe-integer@deno/mod.js';
```
The previous example will load the latest bundled code from the deno branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/constants-float16-min-safe-integer/tags). For example,

```javascript
import FLOAT16_MIN_SAFE_INTEGER from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float16-min-safe-integer@v0.2.0-deno/mod.js';
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
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@deno/mod.js';
import round from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-round@deno/mod.js';
import pow from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-pow@deno/mod.js';
import FLOAT16_MIN_SAFE_INTEGER from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float16-min-safe-integer@deno/mod.js';

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

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/constants-float16/max-safe-integer`][@stdlib/constants/float16/max-safe-integer]</span><span class="delimiter">: </span><span class="description">maximum safe half-precision floating-point integer.</span>
-   <span class="package-name">[`@stdlib/constants-float32/min-safe-integer`][@stdlib/constants/float32/min-safe-integer]</span><span class="delimiter">: </span><span class="description">minimum safe single-precision floating-point integer.</span>
-   <span class="package-name">[`@stdlib/constants-float64/min-safe-integer`][@stdlib/constants/float64/min-safe-integer]</span><span class="delimiter">: </span><span class="description">minimum safe double-precision floating-point integer.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float16-min-safe-integer.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float16-min-safe-integer

[test-image]: https://github.com/stdlib-js/constants-float16-min-safe-integer/actions/workflows/test.yml/badge.svg?branch=v0.2.0
[test-url]: https://github.com/stdlib-js/constants-float16-min-safe-integer/actions/workflows/test.yml?query=branch:v0.2.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float16-min-safe-integer/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float16-min-safe-integer?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float16-min-safe-integer.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float16-min-safe-integer/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/constants-float16-min-safe-integer/tree/deno
[deno-readme]: https://github.com/stdlib-js/constants-float16-min-safe-integer/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/constants-float16-min-safe-integer/tree/umd
[umd-readme]: https://github.com/stdlib-js/constants-float16-min-safe-integer/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/constants-float16-min-safe-integer/tree/esm
[esm-readme]: https://github.com/stdlib-js/constants-float16-min-safe-integer/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/constants-float16-min-safe-integer/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float16-min-safe-integer/main/LICENSE

[safe-integers]: http://www.2ality.com/2013/10/safe-integers.html

[half-precision-floating-point-format]: https://en.wikipedia.org/wiki/Half-precision_floating-point_format

<!-- <related-links> -->

[@stdlib/constants/float16/max-safe-integer]: https://github.com/stdlib-js/constants-float16-max-safe-integer/tree/deno

[@stdlib/constants/float32/min-safe-integer]: https://github.com/stdlib-js/constants-float32-min-safe-integer/tree/deno

[@stdlib/constants/float64/min-safe-integer]: https://github.com/stdlib-js/constants-float64-min-safe-integer/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
