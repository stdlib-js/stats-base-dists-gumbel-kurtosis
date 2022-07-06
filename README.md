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

# Kurtosis

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Gumbel][gumbel-distribution] distribution [excess kurtosis][kurtosis].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [excess kurtosis][kurtosis] for a [Gumbel][gumbel-distribution] random variable with location `μ` and scale `β` is

<!-- <equation class="equation" label="eq:gumbel_kurtosis" align="center" raw="\operatorname{Kurt}\left( X \right) = \frac{12}{5}" alt="Excess kurtosis for a Gumbel distribution."> -->

<div class="equation" align="center" data-raw-text="\operatorname{Kurt}\left( X \right) = \frac{12}{5}" data-equation="eq:gumbel_kurtosis">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/gumbel/kurtosis/docs/img/equation_gumbel_kurtosis.svg" alt="Excess kurtosis for a Gumbel distribution.">
    <br>
</div>

<!-- </equation> -->

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
kurtosis = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-gumbel-kurtosis@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var kurtosis = require( 'path/to/vendor/umd/stats-base-dists-gumbel-kurtosis/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-gumbel-kurtosis@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.kurtosis;
})();
</script>
```

#### kurtosis( mu, beta )

Returns the [excess kurtosis][kurtosis] for a [Gumbel][gumbel-distribution] distribution with location parameter `mu` and scale parameter `beta`.

```javascript
var y = kurtosis( 2.0, 1.0 );
// returns 2.4

y = kurtosis( 0.0, 1.0 );
// returns 2.4

y = kurtosis( -1.0, 4.0 );
// returns 2.4
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var y = kurtosis( NaN, 1.0 );
// returns NaN

y = kurtosis( 0.0, NaN );
// returns NaN
```

If provided `beta <= 0`, the function returns `NaN`.

```javascript
var y = kurtosis( 0.0, 0.0 );
// returns NaN

y = kurtosis( 0.0, -1.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-gumbel-kurtosis@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var beta;
var mu;
var y;
var i;

for ( i = 0; i < 10; i++ ) {
    mu = ( randu()*10.0 ) - 5.0;
    beta = randu() * 20.0;
    y = kurtosis( mu, beta );
    console.log( 'µ: %d, β: %d, Kurt(X;µ,β): %d', mu.toFixed( 4 ), beta.toFixed( 4 ), y.toFixed( 4 ) );
}

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-gumbel-kurtosis.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-gumbel-kurtosis

[test-image]: https://github.com/stdlib-js/stats-base-dists-gumbel-kurtosis/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/stats-base-dists-gumbel-kurtosis/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-gumbel-kurtosis/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-gumbel-kurtosis?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-gumbel-kurtosis.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-gumbel-kurtosis/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-gumbel-kurtosis/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-gumbel-kurtosis/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-gumbel-kurtosis/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-base-dists-gumbel-kurtosis/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-gumbel-kurtosis/main/LICENSE

[gumbel-distribution]: https://en.wikipedia.org/wiki/Gumbel_distribution

[kurtosis]: https://en.wikipedia.org/wiki/Kurtosis

</section>

<!-- /.links -->
