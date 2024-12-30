<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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

# FLOAT32_ABS_MASK

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Mask for excluding the sign bit of a [single-precision floating-point number][ieee754].



<section class="usage">

## Usage

```javascript
import FLOAT32_ABS_MASK from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-abs-mask@esm/index.mjs';
```

#### FLOAT32_ABS_MASK

Mask for excluding the sign bit of a [single-precision floating-point number][ieee754].

```javascript
// 0x7fffffff = 2147483647 => 0 11111111 11111111111111111111111
var bool = ( FLOAT32_ABS_MASK === 0x7fffffff );
// returns true
```

</section>

<!-- /.usage -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import toWord from 'https://cdn.jsdelivr.net/gh/stdlib-js/number-float32-base-to-word@esm/index.mjs';
import fromWord from 'https://cdn.jsdelivr.net/gh/stdlib-js/number-float32-base-from-word@esm/index.mjs';
import FLOAT32_ABS_MASK from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-float32-abs-mask@esm/index.mjs';

var x = -11.5;
var w = toWord( x ); // 1 10000010 01110000000000000000000
// returns 3223781376

// Turn off the sign bit and leave other bits unchanged:
var out = w & FLOAT32_ABS_MASK; // 0 10000010 01110000000000000000000
// returns 1076297728

// Generate a new value:
out = fromWord( out );
// returns 11.5

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/constants-float32/exponent-mask`][@stdlib/constants/float32/exponent-mask]</span><span class="delimiter">: </span><span class="description">mask for the exponent of a single-precision floating-point number.</span>
-   <span class="package-name">[`@stdlib/constants-float32/sign-mask`][@stdlib/constants/float32/sign-mask]</span><span class="delimiter">: </span><span class="description">mask for the sign bit of a single-precision floating-point number.</span>
-   <span class="package-name">[`@stdlib/constants-float32/significand-mask`][@stdlib/constants/float32/significand-mask]</span><span class="delimiter">: </span><span class="description">mask for the significand of a single-precision floating-point number.</span>

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/constants-float32-abs-mask.svg
[npm-url]: https://npmjs.org/package/@stdlib/constants-float32-abs-mask

[test-image]: https://github.com/stdlib-js/constants-float32-abs-mask/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/constants-float32-abs-mask/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/constants-float32-abs-mask/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/constants-float32-abs-mask?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/constants-float32-abs-mask.svg
[dependencies-url]: https://david-dm.org/stdlib-js/constants-float32-abs-mask/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/constants-float32-abs-mask/tree/deno
[deno-readme]: https://github.com/stdlib-js/constants-float32-abs-mask/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/constants-float32-abs-mask/tree/umd
[umd-readme]: https://github.com/stdlib-js/constants-float32-abs-mask/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/constants-float32-abs-mask/tree/esm
[esm-readme]: https://github.com/stdlib-js/constants-float32-abs-mask/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/constants-float32-abs-mask/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/constants-float32-abs-mask/main/LICENSE

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

<!-- <related-links> -->

[@stdlib/constants/float32/exponent-mask]: https://github.com/stdlib-js/constants-float32-exponent-mask/tree/esm

[@stdlib/constants/float32/sign-mask]: https://github.com/stdlib-js/constants-float32-sign-mask/tree/esm

[@stdlib/constants/float32/significand-mask]: https://github.com/stdlib-js/constants-float32-significand-mask/tree/esm

<!-- </related-links> -->

</section>

<!-- /.links -->
