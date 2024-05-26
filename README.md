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

# Assert

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Assertion utilities.

<section class="installation">

## Installation

```bash
npm install @taktikorg/ipsum-aperiam
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var assert = require( '@taktikorg/ipsum-aperiam' );
```

#### assert

Namespace providing utilities for data type testing and feature detection.

```javascript
var o = assert;
// returns {...}
```

To validate the built-in JavaScript data types, the namespace includes the following assertion utilities:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArray( value )`][@taktikorg/ipsum-aperiam/is-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array.</span>
-   <span class="signature">[`isBoolean( value )`][@taktikorg/ipsum-aperiam/is-boolean]</span><span class="delimiter">: </span><span class="description">test if a value is a boolean.</span>
-   <span class="signature">[`isDateObject( value )`][@taktikorg/ipsum-aperiam/is-date-object]</span><span class="delimiter">: </span><span class="description">test if a value is a Date object.</span>
-   <span class="signature">[`isFunction( value )`][@taktikorg/ipsum-aperiam/is-function]</span><span class="delimiter">: </span><span class="description">test if a value is a function.</span>
-   <span class="signature">[`isnan( value )`][@taktikorg/ipsum-aperiam/is-nan]</span><span class="delimiter">: </span><span class="description">test if a value is NaN.</span>
-   <span class="signature">[`isNull( value )`][@taktikorg/ipsum-aperiam/is-null]</span><span class="delimiter">: </span><span class="description">test if a value is null.</span>
-   <span class="signature">[`isNumber( value )`][@taktikorg/ipsum-aperiam/is-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number.</span>
-   <span class="signature">[`isObject( value )`][@taktikorg/ipsum-aperiam/is-object]</span><span class="delimiter">: </span><span class="description">test if a value is an object.</span>
-   <span class="signature">[`isRegExp( value )`][@taktikorg/ipsum-aperiam/is-regexp]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression.</span>
-   <span class="signature">[`isString( value )`][@taktikorg/ipsum-aperiam/is-string]</span><span class="delimiter">: </span><span class="description">test if a value is a string.</span>
-   <span class="signature">[`isSymbol( value )`][@taktikorg/ipsum-aperiam/is-symbol]</span><span class="delimiter">: </span><span class="description">test if a value is a symbol.</span>
-   <span class="signature">[`isUndefined( value )`][@taktikorg/ipsum-aperiam/is-undefined]</span><span class="delimiter">: </span><span class="description">test if a value is undefined.</span>

</div>

<!-- </toc> -->

For primitive types having corresponding object wrappers, assertion utilities provide `isObject` and `isPrimitive` methods to test for either objects or primitives, respectively.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Boolean = require( '@stdlib/boolean/ctor' );
var isBoolean = require( '@taktikorg/ipsum-aperiam/is-boolean' );

var bool = isBoolean.isObject( new Boolean( false ) );
// returns true

bool = isBoolean.isObject( false );
// returns false

bool = isBoolean.isPrimitive( false );
// returns true
```

Many of the assertion utilities have corresponding packages that test whether array elements are of the given data type:

<!-- <toc pattern="is-+(array|boolean|date-object|function|string|nan|number|object|regexp|symbol|null|undefined)-array" > -->

<div class="namespace-toc">

-   <span class="signature">[`isArrayArray( value )`][@taktikorg/ipsum-aperiam/is-array-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of arrays.</span>
-   <span class="signature">[`isBooleanArray( value )`][@taktikorg/ipsum-aperiam/is-boolean-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of booleans.</span>
-   <span class="signature">[`isDateObjectArray( value )`][@taktikorg/ipsum-aperiam/is-date-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only Date objects.</span>
-   <span class="signature">[`isFunctionArray( value )`][@taktikorg/ipsum-aperiam/is-function-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only functions.</span>
-   <span class="signature">[`isNaNArray( value )`][@taktikorg/ipsum-aperiam/is-nan-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only NaN values.</span>
-   <span class="signature">[`isNullArray( value )`][@taktikorg/ipsum-aperiam/is-null-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only null values.</span>
-   <span class="signature">[`isNumberArray( value )`][@taktikorg/ipsum-aperiam/is-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object of numbers.</span>
-   <span class="signature">[`isObjectArray( value )`][@taktikorg/ipsum-aperiam/is-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only objects.</span>
-   <span class="signature">[`isStringArray( value )`][@taktikorg/ipsum-aperiam/is-string-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of strings.</span>
-   <span class="signature">[`isSymbolArray( value )`][@taktikorg/ipsum-aperiam/is-symbol-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only symbols.</span>

</div>

<!-- </toc> -->

Where applicable, similar to the assertion utilities for built-in data types, array assertion utilities provides methods for testing for an array of primitives or objects.

<!-- eslint-disable no-new-wrappers -->

```javascript
var isStringArray = require( '@taktikorg/ipsum-aperiam/is-string-array' );

var bool = isStringArray( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.primitives( [ 'hello', 'world' ] );
// returns true

bool = isStringArray.objects( [ 'hello', 'world' ] );
// returns false

bool = isStringArray.objects( [ new String( 'hello' ), new String( 'world' ) ] );
// returns true
```

The namespace also contains utilities to test for numbers within a certain range or for numbers satisfying a particular "type":

<!-- <toc pattern="is-*+(number|integer)*" ignore="is-number-array" ignore="is-number" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCubeNumber( value )`][@taktikorg/ipsum-aperiam/is-cube-number]</span><span class="delimiter">: </span><span class="description">test if a value is a cube number.</span>
-   <span class="signature">[`isIntegerArray( value )`][@taktikorg/ipsum-aperiam/is-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only integers.</span>
-   <span class="signature">[`isInteger( value )`][@taktikorg/ipsum-aperiam/is-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having an integer value.</span>
-   <span class="signature">[`isNegativeIntegerArray( value )`][@taktikorg/ipsum-aperiam/is-negative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative integers.</span>
-   <span class="signature">[`isNegativeInteger( value )`][@taktikorg/ipsum-aperiam/is-negative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative integer value.</span>
-   <span class="signature">[`isNegativeNumberArray( value )`][@taktikorg/ipsum-aperiam/is-negative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only negative numbers.</span>
-   <span class="signature">[`isNegativeNumber( value )`][@taktikorg/ipsum-aperiam/is-negative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a negative value.</span>
-   <span class="signature">[`isNonNegativeIntegerArray( value )`][@taktikorg/ipsum-aperiam/is-nonnegative-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative integers.</span>
-   <span class="signature">[`isNonNegativeInteger( value )`][@taktikorg/ipsum-aperiam/is-nonnegative-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative integer value.</span>
-   <span class="signature">[`isNonNegativeNumberArray( value )`][@taktikorg/ipsum-aperiam/is-nonnegative-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonnegative numbers.</span>
-   <span class="signature">[`isNonNegativeNumber( value )`][@taktikorg/ipsum-aperiam/is-nonnegative-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative value.</span>
-   <span class="signature">[`isNonPositiveIntegerArray( value )`][@taktikorg/ipsum-aperiam/is-nonpositive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive integers.</span>
-   <span class="signature">[`isNonPositiveInteger( value )`][@taktikorg/ipsum-aperiam/is-nonpositive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive integer value.</span>
-   <span class="signature">[`isNonPositiveNumberArray( value )`][@taktikorg/ipsum-aperiam/is-nonpositive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only nonpositive numbers.</span>
-   <span class="signature">[`isNonPositiveNumber( value )`][@taktikorg/ipsum-aperiam/is-nonpositive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonpositive value.</span>
-   <span class="signature">[`isPositiveIntegerArray( value )`][@taktikorg/ipsum-aperiam/is-positive-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive integers.</span>
-   <span class="signature">[`isPositiveInteger( value )`][@taktikorg/ipsum-aperiam/is-positive-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive integer value.</span>
-   <span class="signature">[`isPositiveNumberArray( value )`][@taktikorg/ipsum-aperiam/is-positive-number-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only positive numbers.</span>
-   <span class="signature">[`isPositiveNumber( value )`][@taktikorg/ipsum-aperiam/is-positive-number]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a positive value.</span>
-   <span class="signature">[`isSafeIntegerArray( value )`][@taktikorg/ipsum-aperiam/is-safe-integer-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only safe integers.</span>
-   <span class="signature">[`isSafeInteger( value )`][@taktikorg/ipsum-aperiam/is-safe-integer]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a safe integer value.</span>
-   <span class="signature">[`isSquareNumber( value )`][@taktikorg/ipsum-aperiam/is-square-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square number.</span>
-   <span class="signature">[`isSquareTriangularNumber( value )`][@taktikorg/ipsum-aperiam/is-square-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a square triangular number.</span>
-   <span class="signature">[`isTriangularNumber( value )`][@taktikorg/ipsum-aperiam/is-triangular-number]</span><span class="delimiter">: </span><span class="description">test if a value is a triangular number.</span>

</div>

<!-- </toc> -->

The namespace provides utilities for validating typed arrays:

<!-- <toc pattern="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array"> -->

<div class="namespace-toc">

-   <span class="signature">[`isFloat32Array( value )`][@taktikorg/ipsum-aperiam/is-float32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float32Array.</span>
-   <span class="signature">[`isFloat64Array( value )`][@taktikorg/ipsum-aperiam/is-float64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Float64Array.</span>
-   <span class="signature">[`isInt16Array( value )`][@taktikorg/ipsum-aperiam/is-int16array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int16Array.</span>
-   <span class="signature">[`isInt32Array( value )`][@taktikorg/ipsum-aperiam/is-int32array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int32Array.</span>
-   <span class="signature">[`isInt8Array( value )`][@taktikorg/ipsum-aperiam/is-int8array]</span><span class="delimiter">: </span><span class="description">test if a value is an Int8Array.</span>
-   <span class="signature">[`isUint16Array( value )`][@taktikorg/ipsum-aperiam/is-uint16array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint16Array.</span>
-   <span class="signature">[`isUint32Array( value )`][@taktikorg/ipsum-aperiam/is-uint32array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint32Array.</span>
-   <span class="signature">[`isUint8Array( value )`][@taktikorg/ipsum-aperiam/is-uint8array]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8Array.</span>
-   <span class="signature">[`isUint8ClampedArray( value )`][@taktikorg/ipsum-aperiam/is-uint8clampedarray]</span><span class="delimiter">: </span><span class="description">test if a value is a Uint8ClampedArray.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating `ndarray`s (n-dimensional arrays).

<!-- <toc keywords="+ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isCentrosymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a centrosymmetric matrix.</span>
-   <span class="signature">[`isComplex128MatrixLike( value )`][@taktikorg/ipsum-aperiam/is-complex128matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128ndarrayLike( value )`][@taktikorg/ipsum-aperiam/is-complex128ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex128VectorLike( value )`][@taktikorg/ipsum-aperiam/is-complex128vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64MatrixLike( value )`][@taktikorg/ipsum-aperiam/is-complex64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64ndarrayLike( value )`][@taktikorg/ipsum-aperiam/is-complex64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isComplex64VectorLike( value )`][@taktikorg/ipsum-aperiam/is-complex64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision complex floating-point numbers.</span>
-   <span class="signature">[`isFloat32MatrixLike( value )`][@taktikorg/ipsum-aperiam/is-float32matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32ndarrayLike( value )`][@taktikorg/ipsum-aperiam/is-float32ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat32VectorLike( value )`][@taktikorg/ipsum-aperiam/is-float32vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing single-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64MatrixLike( value )`][@taktikorg/ipsum-aperiam/is-float64matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64ndarrayLike( value )`][@taktikorg/ipsum-aperiam/is-float64ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is an ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isFloat64VectorLike( value )`][@taktikorg/ipsum-aperiam/is-float64vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object containing double-precision floating-point numbers.</span>
-   <span class="signature">[`isMatrixLike( value )`][@taktikorg/ipsum-aperiam/is-matrix-like]</span><span class="delimiter">: </span><span class="description">test if a value is 2-dimensional ndarray-like object.</span>
-   <span class="signature">[`isndarrayLike( value )`][@taktikorg/ipsum-aperiam/is-ndarray-like]</span><span class="delimiter">: </span><span class="description">test if a value is ndarray-like.</span>
-   <span class="signature">[`isNonSymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-nonsymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a non-symmetric matrix.</span>
-   <span class="signature">[`isPersymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a persymmetric matrix.</span>
-   <span class="signature">[`isSkewCentrosymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-skew-centrosymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-centrosymmetric matrix.</span>
-   <span class="signature">[`isSkewPersymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-skew-persymmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-persymmetric matrix.</span>
-   <span class="signature">[`isSkewSymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-skew-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a skew-symmetric matrix.</span>
-   <span class="signature">[`isSquareMatrix( value )`][@taktikorg/ipsum-aperiam/is-square-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a 2-dimensional ndarray-like object having equal dimensions.</span>
-   <span class="signature">[`isSymmetricMatrix( value )`][@taktikorg/ipsum-aperiam/is-symmetric-matrix]</span><span class="delimiter">: </span><span class="description">test if a value is a symmetric matrix.</span>
-   <span class="signature">[`isVectorLike( value )`][@taktikorg/ipsum-aperiam/is-vector-like]</span><span class="delimiter">: </span><span class="description">test if a value is a 1-dimensional ndarray-like object.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating complex numbers and arrays of complex numbers:

<!-- <toc pattern="is-complex*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isComplexLike( value )`][@taktikorg/ipsum-aperiam/is-complex-like]</span><span class="delimiter">: </span><span class="description">test if a value is a complex number-like object.</span>
-   <span class="signature">[`isComplexTypedArrayLike( value )`][@taktikorg/ipsum-aperiam/is-complex-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is complex-typed-array-like.</span>
-   <span class="signature">[`isComplexTypedArray( value )`][@taktikorg/ipsum-aperiam/is-complex-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a complex typed array.</span>
-   <span class="signature">[`isComplex( value )`][@taktikorg/ipsum-aperiam/is-complex]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit or 128-bit complex number.</span>
-   <span class="signature">[`isComplex128( value )`][@taktikorg/ipsum-aperiam/is-complex128]</span><span class="delimiter">: </span><span class="description">test if a value is a 128-bit complex number.</span>
-   <span class="signature">[`isComplex128Array( value )`][@taktikorg/ipsum-aperiam/is-complex128array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex128Array.</span>
-   <span class="signature">[`isComplex64( value )`][@taktikorg/ipsum-aperiam/is-complex64]</span><span class="delimiter">: </span><span class="description">test if a value is a 64-bit complex number.</span>
-   <span class="signature">[`isComplex64Array( value )`][@taktikorg/ipsum-aperiam/is-complex64array]</span><span class="delimiter">: </span><span class="description">test if a value is a Complex64Array.</span>

</div>

<!-- </toc> -->

The namespace includes utilities for validating other special arrays or buffers:

<!-- <toc pattern="is-*array*" ignore="is-+(int8|int16|int32|uint8clamped|uint8|uint16|uint32|float32|float64)array" ignore="is-*+(number|integer)*" ignore="is-+(array|boolean|date-object|function|string|nan|number|object|primitive|regexp|symbol|null|undefined)-array" ignore="is-array" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`isAccessorArray( value )`][@taktikorg/ipsum-aperiam/is-accessor-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object supporting the accessor (get/set) protocol.</span>
-   <span class="signature">[`isArrayLength( value )`][@taktikorg/ipsum-aperiam/is-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid array length.</span>
-   <span class="signature">[`isArrayLikeObject( value )`][@taktikorg/ipsum-aperiam/is-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object.</span>
-   <span class="signature">[`isArrayLike( value )`][@taktikorg/ipsum-aperiam/is-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is array-like.</span>
-   <span class="signature">[`isArrayBufferView( value )`][@taktikorg/ipsum-aperiam/is-arraybuffer-view]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer view.</span>
-   <span class="signature">[`isArrayBuffer( value )`][@taktikorg/ipsum-aperiam/is-arraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is an ArrayBuffer.</span>
-   <span class="signature">[`isBetweenArray( value, a, b[, left, right] )`][@taktikorg/ipsum-aperiam/is-between-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object where every element is between two values.</span>
-   <span class="signature">[`isBigInt64Array( value )`][@taktikorg/ipsum-aperiam/is-bigint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt64Array.</span>
-   <span class="signature">[`isBigUint64Array( value )`][@taktikorg/ipsum-aperiam/is-biguint64array]</span><span class="delimiter">: </span><span class="description">test if a value is a BigUint64Array.</span>
-   <span class="signature">[`isCircularArray( value )`][@taktikorg/ipsum-aperiam/is-circular-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array containing a circular reference.</span>
-   <span class="signature">[`isEmptyArrayLikeObject( value )`][@taktikorg/ipsum-aperiam/is-empty-array-like-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array-like object.</span>
-   <span class="signature">[`isEmptyArray( value )`][@taktikorg/ipsum-aperiam/is-empty-array]</span><span class="delimiter">: </span><span class="description">test if a value is an empty array.</span>
-   <span class="signature">[`isFalsyArray( value )`][@taktikorg/ipsum-aperiam/is-falsy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only falsy values.</span>
-   <span class="signature">[`isFiniteArray( value )`][@taktikorg/ipsum-aperiam/is-finite-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only finite numbers.</span>
-   <span class="signature">[`isNumericArray( value )`][@taktikorg/ipsum-aperiam/is-numeric-array]</span><span class="delimiter">: </span><span class="description">test if a value is a numeric array.</span>
-   <span class="signature">[`isPlainObjectArray( value )`][@taktikorg/ipsum-aperiam/is-plain-object-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only plain objects.</span>
-   <span class="signature">[`isProbabilityArray( value )`][@taktikorg/ipsum-aperiam/is-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only probabilities.</span>
-   <span class="signature">[`isSameArray( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both generic arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex128Array( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-complex128array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex128Arrays and have the same values.</span>
-   <span class="signature">[`isSameComplex64Array( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-complex64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Complex64Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat32Array( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-float32array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float32Arrays and have the same values.</span>
-   <span class="signature">[`isSameFloat64Array( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-float64array]</span><span class="delimiter">: </span><span class="description">test if two arguments are both Float64Arrays and have the same values.</span>
-   <span class="signature">[`isSharedArrayBuffer( value )`][@taktikorg/ipsum-aperiam/is-sharedarraybuffer]</span><span class="delimiter">: </span><span class="description">test if a value is a SharedArrayBuffer.</span>
-   <span class="signature">[`isTruthyArray( value )`][@taktikorg/ipsum-aperiam/is-truthy-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array-like object containing only truthy values.</span>
-   <span class="signature">[`isTypedArrayLength( value )`][@taktikorg/ipsum-aperiam/is-typed-array-length]</span><span class="delimiter">: </span><span class="description">test if a value is a valid typed array length.</span>
-   <span class="signature">[`isTypedArrayLike( value )`][@taktikorg/ipsum-aperiam/is-typed-array-like]</span><span class="delimiter">: </span><span class="description">test if a value is typed-array-like.</span>
-   <span class="signature">[`isTypedArray( value )`][@taktikorg/ipsum-aperiam/is-typed-array]</span><span class="delimiter">: </span><span class="description">test if a value is a typed array.</span>
-   <span class="signature">[`isUnityProbabilityArray( value )`][@taktikorg/ipsum-aperiam/is-unity-probability-array]</span><span class="delimiter">: </span><span class="description">test if a value is an array of probabilities that sum to one.</span>

</div>

<!-- </toc> -->

To test for error objects, the namespace includes the following utilities:

<!-- <toc pattern="is-*error*" > -->

<div class="namespace-toc">

-   <span class="signature">[`isError( value )`][@taktikorg/ipsum-aperiam/is-error]</span><span class="delimiter">: </span><span class="description">test if a value is an Error object.</span>
-   <span class="signature">[`isEvalError( value )`][@taktikorg/ipsum-aperiam/is-eval-error]</span><span class="delimiter">: </span><span class="description">test if a value is an EvalError object.</span>
-   <span class="signature">[`isRangeError( value )`][@taktikorg/ipsum-aperiam/is-range-error]</span><span class="delimiter">: </span><span class="description">test if a value is a RangeError object.</span>
-   <span class="signature">[`isReferenceError( value )`][@taktikorg/ipsum-aperiam/is-reference-error]</span><span class="delimiter">: </span><span class="description">test if a value is a ReferenceError object.</span>
-   <span class="signature">[`isSyntaxError( value )`][@taktikorg/ipsum-aperiam/is-syntax-error]</span><span class="delimiter">: </span><span class="description">test if a value is a SyntaxError object.</span>
-   <span class="signature">[`isTypeError( value )`][@taktikorg/ipsum-aperiam/is-type-error]</span><span class="delimiter">: </span><span class="description">test if a value is a TypeError object.</span>
-   <span class="signature">[`isURIError( value )`][@taktikorg/ipsum-aperiam/is-uri-error]</span><span class="delimiter">: </span><span class="description">test if a value is a URIError object.</span>

</div>

<!-- </toc> -->

The namespace exposes the following constants concerning the current running process:

<!-- <toc pattern="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|big-endian|node|web-worker|windows|docker|mobile|touch-device)" > -->

<div class="namespace-toc">

-   <span class="signature">[`IS_BIG_ENDIAN`][@taktikorg/ipsum-aperiam/is-big-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is big endian.</span>
-   <span class="signature">[`IS_BROWSER`][@taktikorg/ipsum-aperiam/is-browser]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web browser.</span>
-   <span class="signature">[`IS_DARWIN`][@taktikorg/ipsum-aperiam/is-darwin]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Darwin.</span>
-   <span class="signature">[`IS_DOCKER`][@taktikorg/ipsum-aperiam/is-docker]</span><span class="delimiter">: </span><span class="description">check if the process is running in a Docker container.</span>
-   <span class="signature">[`IS_ELECTRON_MAIN`][@taktikorg/ipsum-aperiam/is-electron-main]</span><span class="delimiter">: </span><span class="description">check if the runtime is the main Electron process.</span>
-   <span class="signature">[`IS_ELECTRON_RENDERER`][@taktikorg/ipsum-aperiam/is-electron-renderer]</span><span class="delimiter">: </span><span class="description">check if the runtime is the Electron renderer process.</span>
-   <span class="signature">[`IS_ELECTRON`][@taktikorg/ipsum-aperiam/is-electron]</span><span class="delimiter">: </span><span class="description">check if the runtime is Electron.</span>
-   <span class="signature">[`IS_LITTLE_ENDIAN`][@taktikorg/ipsum-aperiam/is-little-endian]</span><span class="delimiter">: </span><span class="description">check if an environment is little endian.</span>
-   <span class="signature">[`IS_MOBILE`][@taktikorg/ipsum-aperiam/is-mobile]</span><span class="delimiter">: </span><span class="description">check if the current environment is a mobile device.</span>
-   <span class="signature">[`IS_NODE`][@taktikorg/ipsum-aperiam/is-node]</span><span class="delimiter">: </span><span class="description">check if the runtime is Node.js.</span>
-   <span class="signature">[`IS_TOUCH_DEVICE`][@taktikorg/ipsum-aperiam/is-touch-device]</span><span class="delimiter">: </span><span class="description">check if the current environment is a touch device.</span>
-   <span class="signature">[`IS_WEB_WORKER`][@taktikorg/ipsum-aperiam/is-web-worker]</span><span class="delimiter">: </span><span class="description">check if the runtime is a web worker.</span>
-   <span class="signature">[`IS_WINDOWS`][@taktikorg/ipsum-aperiam/is-windows]</span><span class="delimiter">: </span><span class="description">boolean indicating if the current process is running on Windows.</span>

</div>

<!-- </toc> -->

To test whether a runtime environment supports certain features, the namespace includes the following utilities:

<!-- <toc pattern="has-*-support" > -->

<div class="namespace-toc">

-   <span class="signature">[`hasArrayBufferSupport()`][@taktikorg/ipsum-aperiam/has-arraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `ArrayBuffer` support.</span>
-   <span class="signature">[`hasArrowFunctionSupport()`][@taktikorg/ipsum-aperiam/has-arrow-function-support]</span><span class="delimiter">: </span><span class="description">detect native `arrow function` support.</span>
-   <span class="signature">[`hasAsyncAwaitSupport()`][@taktikorg/ipsum-aperiam/has-async-await-support]</span><span class="delimiter">: </span><span class="description">detect native `async`/`await` support.</span>
-   <span class="signature">[`hasAsyncIteratorSymbolSupport()`][@taktikorg/ipsum-aperiam/has-async-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.asyncIterator` support.</span>
-   <span class="signature">[`hasBigIntSupport()`][@taktikorg/ipsum-aperiam/has-bigint-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt` support.</span>
-   <span class="signature">[`hasBigInt64ArraySupport()`][@taktikorg/ipsum-aperiam/has-bigint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigInt64Array` support.</span>
-   <span class="signature">[`hasBigUint64ArraySupport()`][@taktikorg/ipsum-aperiam/has-biguint64array-support]</span><span class="delimiter">: </span><span class="description">detect native `BigUint64Array` support.</span>
-   <span class="signature">[`hasClassSupport()`][@taktikorg/ipsum-aperiam/has-class-support]</span><span class="delimiter">: </span><span class="description">detect native `class` support.</span>
-   <span class="signature">[`hasDataViewSupport()`][@taktikorg/ipsum-aperiam/has-dataview-support]</span><span class="delimiter">: </span><span class="description">detect native `DataView` support.</span>
-   <span class="signature">[`hasDefinePropertiesSupport()`][@taktikorg/ipsum-aperiam/has-define-properties-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperties` support.</span>
-   <span class="signature">[`hasDefinePropertySupport()`][@taktikorg/ipsum-aperiam/has-define-property-support]</span><span class="delimiter">: </span><span class="description">detect `Object.defineProperty` support.</span>
-   <span class="signature">[`hasFloat32ArraySupport()`][@taktikorg/ipsum-aperiam/has-float32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float32Array` support.</span>
-   <span class="signature">[`hasFloat64ArraySupport()`][@taktikorg/ipsum-aperiam/has-float64array-support]</span><span class="delimiter">: </span><span class="description">detect native `Float64Array` support.</span>
-   <span class="signature">[`hasFunctionNameSupport()`][@taktikorg/ipsum-aperiam/has-function-name-support]</span><span class="delimiter">: </span><span class="description">detect native function `name` support.</span>
-   <span class="signature">[`hasGeneratorSupport()`][@taktikorg/ipsum-aperiam/has-generator-support]</span><span class="delimiter">: </span><span class="description">detect native `generator function` support.</span>
-   <span class="signature">[`hasGlobalThisSupport()`][@taktikorg/ipsum-aperiam/has-globalthis-support]</span><span class="delimiter">: </span><span class="description">detect `globalThis` support.</span>
-   <span class="signature">[`hasInt16ArraySupport()`][@taktikorg/ipsum-aperiam/has-int16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int16Array` support.</span>
-   <span class="signature">[`hasInt32ArraySupport()`][@taktikorg/ipsum-aperiam/has-int32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int32Array` support.</span>
-   <span class="signature">[`hasInt8ArraySupport()`][@taktikorg/ipsum-aperiam/has-int8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Int8Array` support.</span>
-   <span class="signature">[`hasIteratorSymbolSupport()`][@taktikorg/ipsum-aperiam/has-iterator-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.iterator` support.</span>
-   <span class="signature">[`hasMapSupport()`][@taktikorg/ipsum-aperiam/has-map-support]</span><span class="delimiter">: </span><span class="description">detect native `Map` support.</span>
-   <span class="signature">[`hasNodeBufferSupport()`][@taktikorg/ipsum-aperiam/has-node-buffer-support]</span><span class="delimiter">: </span><span class="description">detect native `Buffer` support.</span>
-   <span class="signature">[`hasProxySupport()`][@taktikorg/ipsum-aperiam/has-proxy-support]</span><span class="delimiter">: </span><span class="description">detect native `Proxy` support.</span>
-   <span class="signature">[`hasSetSupport()`][@taktikorg/ipsum-aperiam/has-set-support]</span><span class="delimiter">: </span><span class="description">detect native `Set` support.</span>
-   <span class="signature">[`hasSharedArrayBufferSupport()`][@taktikorg/ipsum-aperiam/has-sharedarraybuffer-support]</span><span class="delimiter">: </span><span class="description">detect native `SharedArrayBuffer` support.</span>
-   <span class="signature">[`hasSymbolSupport()`][@taktikorg/ipsum-aperiam/has-symbol-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol` support.</span>
-   <span class="signature">[`hasToStringTagSupport()`][@taktikorg/ipsum-aperiam/has-tostringtag-support]</span><span class="delimiter">: </span><span class="description">detect native `Symbol.toStringTag` support.</span>
-   <span class="signature">[`hasUint16ArraySupport()`][@taktikorg/ipsum-aperiam/has-uint16array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint16Array` support.</span>
-   <span class="signature">[`hasUint32ArraySupport()`][@taktikorg/ipsum-aperiam/has-uint32array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint32Array` support.</span>
-   <span class="signature">[`hasUint8ArraySupport()`][@taktikorg/ipsum-aperiam/has-uint8array-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8Array` support.</span>
-   <span class="signature">[`hasUint8ClampedArraySupport()`][@taktikorg/ipsum-aperiam/has-uint8clampedarray-support]</span><span class="delimiter">: </span><span class="description">detect native `Uint8ClampedArray` support.</span>
-   <span class="signature">[`hasWebAssemblySupport()`][@taktikorg/ipsum-aperiam/has-wasm-support]</span><span class="delimiter">: </span><span class="description">detect native WebAssembly support.</span>
-   <span class="signature">[`hasWeakMapSupport()`][@taktikorg/ipsum-aperiam/has-weakmap-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakMap` support.</span>
-   <span class="signature">[`hasWeakSetSupport()`][@taktikorg/ipsum-aperiam/has-weakset-support]</span><span class="delimiter">: </span><span class="description">detect native `WeakSet` support.</span>

</div>

<!-- </toc> -->

The remaining namespace utilities are as follows:

<!-- <toc ignore="is-+(array|boolean|date-object|function|string|symbol|nan|null|number|object|regexp|symbol|undefined)" ignore="is-*+(number|integer)*" ignore="is-*array*" ignore="is-*error*" ignore="is-+(browser|darwin|electron|electron-main|electron-renderer|little-endian|node|web-worker|windows)" ignore="has-*-support" keywords="-ndarray" > -->

<div class="namespace-toc">

-   <span class="signature">[`contains( val, searchValue[, position] )`][@taktikorg/ipsum-aperiam/contains]</span><span class="delimiter">: </span><span class="description">test if an array-like value contains a search value.</span>
-   <span class="signature">[`deepEqual( a, b )`][@taktikorg/ipsum-aperiam/deep-equal]</span><span class="delimiter">: </span><span class="description">test for deep equality between two values.</span>
-   <span class="signature">[`deepHasOwnProp( value, path[, options] )`][@taktikorg/ipsum-aperiam/deep-has-own-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path.</span>
-   <span class="signature">[`deepHasProp( value, path[, options] )`][@taktikorg/ipsum-aperiam/deep-has-property]</span><span class="delimiter">: </span><span class="description">test whether an object contains a nested key path, either own or inherited.</span>
-   <span class="signature">[`hasOwnProp( value, property )`][@taktikorg/ipsum-aperiam/has-own-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property.</span>
-   <span class="signature">[`hasProp( value, property )`][@taktikorg/ipsum-aperiam/has-property]</span><span class="delimiter">: </span><span class="description">test if an object has a specified property, either own or inherited.</span>
-   <span class="signature">[`hasUTF16SurrogatePairAt( string, position )`][@taktikorg/ipsum-aperiam/has-utf16-surrogate-pair-at]</span><span class="delimiter">: </span><span class="description">test if a position in a string marks the start of a UTF-16 surrogate pair.</span>
-   <span class="signature">[`instanceOf( value, constructor )`][@taktikorg/ipsum-aperiam/instance-of]</span><span class="delimiter">: </span><span class="description">test whether a value has in its prototype chain a specified constructor as a prototype property.</span>
-   <span class="signature">[`isAbsoluteHttpURI( value )`][@taktikorg/ipsum-aperiam/is-absolute-http-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute HTTP(S) URI.</span>
-   <span class="signature">[`isAbsolutePath( value )`][@taktikorg/ipsum-aperiam/is-absolute-path]</span><span class="delimiter">: </span><span class="description">test if a value is an absolute path.</span>
-   <span class="signature">[`isAbsoluteURI( value )`][@taktikorg/ipsum-aperiam/is-absolute-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is an absolute URI.</span>
-   <span class="signature">[`isAccessorPropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-accessor-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has an accessor descriptor.</span>
-   <span class="signature">[`isAccessorProperty( value, property )`][@taktikorg/ipsum-aperiam/is-accessor-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has an accessor descriptor.</span>
-   <span class="signature">[`isAlphagram( value )`][@taktikorg/ipsum-aperiam/is-alphagram]</span><span class="delimiter">: </span><span class="description">test if a value is an alphagram.</span>
-   <span class="signature">[`isAlphaNumeric( value )`][@taktikorg/ipsum-aperiam/is-alphanumeric]</span><span class="delimiter">: </span><span class="description">test whether a string contains only alphanumeric characters.</span>
-   <span class="signature">[`isAnagram( str, value )`][@taktikorg/ipsum-aperiam/is-anagram]</span><span class="delimiter">: </span><span class="description">test if a value is an anagram.</span>
-   <span class="signature">[`isArguments( value )`][@taktikorg/ipsum-aperiam/is-arguments]</span><span class="delimiter">: </span><span class="description">test if a value is an arguments object.</span>
-   <span class="signature">[`isArrowFunction( value )`][@taktikorg/ipsum-aperiam/is-arrow-function]</span><span class="delimiter">: </span><span class="description">test if a value is an `arrow function`.</span>
-   <span class="signature">[`isASCII( value )`][@taktikorg/ipsum-aperiam/is-ascii]</span><span class="delimiter">: </span><span class="description">test whether a character belongs to the ASCII character set and whether this is true for all characters in a provided string.</span>
-   <span class="signature">[`isBetween( value, a, b[, left, right] )`][@taktikorg/ipsum-aperiam/is-between]</span><span class="delimiter">: </span><span class="description">test if a value is between two values.</span>
-   <span class="signature">[`isBigInt( value )`][@taktikorg/ipsum-aperiam/is-bigint]</span><span class="delimiter">: </span><span class="description">test if a value is a BigInt.</span>
-   <span class="signature">[`isBinaryString( value )`][@taktikorg/ipsum-aperiam/is-binary-string]</span><span class="delimiter">: </span><span class="description">test if a value is a binary string.</span>
-   <span class="signature">[`isBlankString( value )`][@taktikorg/ipsum-aperiam/is-blank-string]</span><span class="delimiter">: </span><span class="description">test if a value is a blank string.</span>
-   <span class="signature">[`isBoxedPrimitive( value )`][@taktikorg/ipsum-aperiam/is-boxed-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript boxed primitive.</span>
-   <span class="signature">[`isBuffer( value )`][@taktikorg/ipsum-aperiam/is-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a Buffer object.</span>
-   <span class="signature">[`isCamelcase( value )`][@taktikorg/ipsum-aperiam/is-camelcase]</span><span class="delimiter">: </span><span class="description">test if a value is a camelcase string.</span>
-   <span class="signature">[`isCapitalized( value )`][@taktikorg/ipsum-aperiam/is-capitalized]</span><span class="delimiter">: </span><span class="description">test if a value is a string having an uppercase first character.</span>
-   <span class="signature">[`isCircular( value )`][@taktikorg/ipsum-aperiam/is-circular]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object containing a circular reference.</span>
-   <span class="signature">[`isCircular( value )`][@taktikorg/ipsum-aperiam/is-circular]</span><span class="delimiter">: </span><span class="description">test if an object-like value contains a circular reference.</span>
-   <span class="signature">[`isClass( value )`][@taktikorg/ipsum-aperiam/is-class]</span><span class="delimiter">: </span><span class="description">test if a value is a class.</span>
-   <span class="signature">[`isCollection( value )`][@taktikorg/ipsum-aperiam/is-collection]</span><span class="delimiter">: </span><span class="description">test if a value is a collection.</span>
-   <span class="signature">[`isComposite( value )`][@taktikorg/ipsum-aperiam/is-composite]</span><span class="delimiter">: </span><span class="description">test if a value is a composite number.</span>
-   <span class="signature">[`isConfigurablePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-configurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is configurable.</span>
-   <span class="signature">[`isConfigurableProperty( value, property )`][@taktikorg/ipsum-aperiam/is-configurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is configurable.</span>
-   <span class="signature">[`isConstantcase( value )`][@taktikorg/ipsum-aperiam/is-constantcase]</span><span class="delimiter">: </span><span class="description">test if a value is a constantcase string.</span>
-   <span class="signature">[`isCurrentYear( value )`][@taktikorg/ipsum-aperiam/is-current-year]</span><span class="delimiter">: </span><span class="description">test if a value is the current year.</span>
-   <span class="signature">[`isDataPropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-data-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property has a data descriptor.</span>
-   <span class="signature">[`isDataProperty( value, property )`][@taktikorg/ipsum-aperiam/is-data-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property has a data descriptor.</span>
-   <span class="signature">[`isDataView( value )`][@taktikorg/ipsum-aperiam/is-dataview]</span><span class="delimiter">: </span><span class="description">test if a value is a DataView.</span>
-   <span class="signature">[`isDigitString( value )`][@taktikorg/ipsum-aperiam/is-digit-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only numeric digits.</span>
-   <span class="signature">[`isDomainName( value )`][@taktikorg/ipsum-aperiam/is-domain-name]</span><span class="delimiter">: </span><span class="description">test if a value is a domain name.</span>
-   <span class="signature">[`isDurationString( value )`][@taktikorg/ipsum-aperiam/is-duration-string]</span><span class="delimiter">: </span><span class="description">test if a value is a duration string.</span>
-   <span class="signature">[`isEmailAddress( value )`][@taktikorg/ipsum-aperiam/is-email-address]</span><span class="delimiter">: </span><span class="description">test if a value is an email address.</span>
-   <span class="signature">[`isEmptyCollection( value )`][@taktikorg/ipsum-aperiam/is-empty-collection]</span><span class="delimiter">: </span><span class="description">test if a value is an empty collection.</span>
-   <span class="signature">[`isEmptyObject( value )`][@taktikorg/ipsum-aperiam/is-empty-object]</span><span class="delimiter">: </span><span class="description">test if a value is an empty object.</span>
-   <span class="signature">[`isEmptyString( value )`][@taktikorg/ipsum-aperiam/is-empty-string]</span><span class="delimiter">: </span><span class="description">test if a value is an empty string.</span>
-   <span class="signature">[`isEnumerablePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-enumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is enumerable.</span>
-   <span class="signature">[`isEnumerableProperty( value, property )`][@taktikorg/ipsum-aperiam/is-enumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is enumerable.</span>
-   <span class="signature">[`isEven( value )`][@taktikorg/ipsum-aperiam/is-even]</span><span class="delimiter">: </span><span class="description">test if a value is an even number.</span>
-   <span class="signature">[`isFalsy( value )`][@taktikorg/ipsum-aperiam/is-falsy]</span><span class="delimiter">: </span><span class="description">test if a value is falsy.</span>
-   <span class="signature">[`isFinite( value )`][@taktikorg/ipsum-aperiam/is-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a finite number.</span>
-   <span class="signature">[`isGeneratorObjectLike( value )`][@taktikorg/ipsum-aperiam/is-generator-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is `generator` object-like.</span>
-   <span class="signature">[`isGeneratorObject( value )`][@taktikorg/ipsum-aperiam/is-generator-object]</span><span class="delimiter">: </span><span class="description">test if a value is a `generator` object.</span>
-   <span class="signature">[`isgzipBuffer( value )`][@taktikorg/ipsum-aperiam/is-gzip-buffer]</span><span class="delimiter">: </span><span class="description">test if a value is a gzip buffer.</span>
-   <span class="signature">[`isHexString( value )`][@taktikorg/ipsum-aperiam/is-hex-string]</span><span class="delimiter">: </span><span class="description">test whether a string contains only hexadecimal digits.</span>
-   <span class="signature">[`isInfinite( value )`][@taktikorg/ipsum-aperiam/is-infinite]</span><span class="delimiter">: </span><span class="description">test if a value is an infinite number.</span>
-   <span class="signature">[`isInheritedProperty( value, property )`][@taktikorg/ipsum-aperiam/is-inherited-property]</span><span class="delimiter">: </span><span class="description">test if an object has an inherited property.</span>
-   <span class="signature">[`isIterableLike( value )`][@taktikorg/ipsum-aperiam/is-iterable-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterable`-like.</span>
-   <span class="signature">[`isIteratorLike( value )`][@taktikorg/ipsum-aperiam/is-iterator-like]</span><span class="delimiter">: </span><span class="description">test if a value is `iterator`-like.</span>
-   <span class="signature">[`isJSON( value )`][@taktikorg/ipsum-aperiam/is-json]</span><span class="delimiter">: </span><span class="description">test if a value is a parseable JSON string.</span>
-   <span class="signature">[`isKebabcase( value )`][@taktikorg/ipsum-aperiam/is-kebabcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in kebab case.</span>
-   <span class="signature">[`isLeapYear( [value] )`][@taktikorg/ipsum-aperiam/is-leap-year]</span><span class="delimiter">: </span><span class="description">test if a value corresponds to a leap year in the Gregorian calendar.</span>
-   <span class="signature">[`isLocalhost( value )`][@taktikorg/ipsum-aperiam/is-localhost]</span><span class="delimiter">: </span><span class="description">test whether a value is a localhost hostname.</span>
-   <span class="signature">[`isLowercase( value )`][@taktikorg/ipsum-aperiam/is-lowercase]</span><span class="delimiter">: </span><span class="description">test if a value is a lowercase string.</span>
-   <span class="signature">[`isMethodIn( value, property )`][@taktikorg/ipsum-aperiam/is-method-in]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name, either own or inherited.</span>
-   <span class="signature">[`isMethod( value, property )`][@taktikorg/ipsum-aperiam/is-method]</span><span class="delimiter">: </span><span class="description">test if an object has a specified method name.</span>
-   <span class="signature">[`isMultiSlice( value )`][@taktikorg/ipsum-aperiam/is-multi-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `MultiSlice`.</span>
-   <span class="signature">[`isNamedTypedTupleLike( value )`][@taktikorg/ipsum-aperiam/is-named-typed-tuple-like]</span><span class="delimiter">: </span><span class="description">test if a value is named typed tuple-like.</span>
-   <span class="signature">[`isNativeFunction( value )`][@taktikorg/ipsum-aperiam/is-native-function]</span><span class="delimiter">: </span><span class="description">test if a value is a native function.</span>
-   <span class="signature">[`isNegativeZero( value )`][@taktikorg/ipsum-aperiam/is-negative-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to negative zero.</span>
-   <span class="signature">[`isNodeBuiltin( value )`][@taktikorg/ipsum-aperiam/is-node-builtin]</span><span class="delimiter">: </span><span class="description">test whether a string matches a Node.js built-in module name.</span>
-   <span class="signature">[`isNodeDuplexStreamLike( value )`][@taktikorg/ipsum-aperiam/is-node-duplex-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node duplex stream-like.</span>
-   <span class="signature">[`isNodeReadableStreamLike( value )`][@taktikorg/ipsum-aperiam/is-node-readable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node readable stream-like.</span>
-   <span class="signature">[`isNodeREPL()`][@taktikorg/ipsum-aperiam/is-node-repl]</span><span class="delimiter">: </span><span class="description">check if running in a Node.js REPL environment.</span>
-   <span class="signature">[`isNodeStreamLike( value )`][@taktikorg/ipsum-aperiam/is-node-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node stream-like.</span>
-   <span class="signature">[`isNodeTransformStreamLike( value )`][@taktikorg/ipsum-aperiam/is-node-transform-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node transform stream-like.</span>
-   <span class="signature">[`isNodeWritableStreamLike( value )`][@taktikorg/ipsum-aperiam/is-node-writable-stream-like]</span><span class="delimiter">: </span><span class="description">test if a value is Node writable stream-like.</span>
-   <span class="signature">[`isNonConfigurablePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-nonconfigurable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-configurable.</span>
-   <span class="signature">[`isNonConfigurableProperty( value, property )`][@taktikorg/ipsum-aperiam/is-nonconfigurable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-configurable.</span>
-   <span class="signature">[`isNonEnumerablePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-nonenumerable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is non-enumerable.</span>
-   <span class="signature">[`isNonEnumerableProperty( value, property )`][@taktikorg/ipsum-aperiam/is-nonenumerable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is non-enumerable.</span>
-   <span class="signature">[`isNonNegativeFinite( value )`][@taktikorg/ipsum-aperiam/is-nonnegative-finite]</span><span class="delimiter">: </span><span class="description">test if a value is a number having a nonnegative finite value.</span>
-   <span class="signature">[`isObjectLike( value )`][@taktikorg/ipsum-aperiam/is-object-like]</span><span class="delimiter">: </span><span class="description">test if a value is object-like.</span>
-   <span class="signature">[`isOdd( value )`][@taktikorg/ipsum-aperiam/is-odd]</span><span class="delimiter">: </span><span class="description">test if a value is an odd number.</span>
-   <span class="signature">[`isPascalcase( value )`][@taktikorg/ipsum-aperiam/is-pascalcase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in Pascal case.</span>
-   <span class="signature">[`isPlainObject( value )`][@taktikorg/ipsum-aperiam/is-plain-object]</span><span class="delimiter">: </span><span class="description">test if a value is a plain object.</span>
-   <span class="signature">[`isPositiveZero( value )`][@taktikorg/ipsum-aperiam/is-positive-zero]</span><span class="delimiter">: </span><span class="description">test if a value is a number equal to positive zero.</span>
-   <span class="signature">[`isPrime( value )`][@taktikorg/ipsum-aperiam/is-prime]</span><span class="delimiter">: </span><span class="description">test if a value is a prime number.</span>
-   <span class="signature">[`isPrimitive( value )`][@taktikorg/ipsum-aperiam/is-primitive]</span><span class="delimiter">: </span><span class="description">test if a value is a JavaScript primitive.</span>
-   <span class="signature">[`isPRNGLike( value )`][@taktikorg/ipsum-aperiam/is-prng-like]</span><span class="delimiter">: </span><span class="description">test if a value is PRNG-like.</span>
-   <span class="signature">[`isProbability( value )`][@taktikorg/ipsum-aperiam/is-probability]</span><span class="delimiter">: </span><span class="description">test if a value is a probability.</span>
-   <span class="signature">[`isPropertyKey( value )`][@taktikorg/ipsum-aperiam/is-property-key]</span><span class="delimiter">: </span><span class="description">test whether a value is a property key.</span>
-   <span class="signature">[`isPrototypeOf( obj, prototype )`][@taktikorg/ipsum-aperiam/is-prototype-of]</span><span class="delimiter">: </span><span class="description">test if an object's prototype chain contains a provided prototype.</span>
-   <span class="signature">[`isReadOnlyPropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-read-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is read-only.</span>
-   <span class="signature">[`isReadOnlyProperty( value, property )`][@taktikorg/ipsum-aperiam/is-read-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is read-only.</span>
-   <span class="signature">[`isReadWritePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-read-write-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable and writable.</span>
-   <span class="signature">[`isReadWriteProperty( value, property )`][@taktikorg/ipsum-aperiam/is-read-write-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable and writable.</span>
-   <span class="signature">[`isReadablePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-readable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is readable.</span>
-   <span class="signature">[`isReadableProperty( value, property )`][@taktikorg/ipsum-aperiam/is-readable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is readable.</span>
-   <span class="signature">[`isRegExpString( value )`][@taktikorg/ipsum-aperiam/is-regexp-string]</span><span class="delimiter">: </span><span class="description">test if a value is a regular expression string.</span>
-   <span class="signature">[`isRelativePath( value )`][@taktikorg/ipsum-aperiam/is-relative-path]</span><span class="delimiter">: </span><span class="description">test if a value is a relative path.</span>
-   <span class="signature">[`isRelativeURI( value )`][@taktikorg/ipsum-aperiam/is-relative-uri]</span><span class="delimiter">: </span><span class="description">test whether a value is a relative URI.</span>
-   <span class="signature">[`isSameComplex128( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-complex128]</span><span class="delimiter">: </span><span class="description">test if two arguments are both double-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameComplex64( v1, v2 )`][@taktikorg/ipsum-aperiam/is-same-complex64]</span><span class="delimiter">: </span><span class="description">test if two arguments are both single-precision complex floating-point numbers and have the same value.</span>
-   <span class="signature">[`isSameNativeClass( a, b )`][@taktikorg/ipsum-aperiam/is-same-native-class]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same native class.</span>
-   <span class="signature">[`isSameType( a, b )`][@taktikorg/ipsum-aperiam/is-same-type]</span><span class="delimiter">: </span><span class="description">test if two arguments have the same type.</span>
-   <span class="signature">[`isSameValueZero( a, b )`][@taktikorg/ipsum-aperiam/is-same-value-zero]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSameValue( a, b )`][@taktikorg/ipsum-aperiam/is-same-value]</span><span class="delimiter">: </span><span class="description">test if two arguments are the same value.</span>
-   <span class="signature">[`isSemVer( value )`][@taktikorg/ipsum-aperiam/is-semver]</span><span class="delimiter">: </span><span class="description">test if a value is a semantic version string.</span>
-   <span class="signature">[`isSlice( value )`][@taktikorg/ipsum-aperiam/is-slice]</span><span class="delimiter">: </span><span class="description">test if a value is a `Slice`.</span>
-   <span class="signature">[`isSnakecase( value )`][@taktikorg/ipsum-aperiam/is-snakecase]</span><span class="delimiter">: </span><span class="description">test if a value is a string in snake case.</span>
-   <span class="signature">[`isStartcase( value )`][@taktikorg/ipsum-aperiam/is-startcase]</span><span class="delimiter">: </span><span class="description">test if a value is a startcase string.</span>
-   <span class="signature">[`isStrictEqual( a, b )`][@taktikorg/ipsum-aperiam/is-strict-equal]</span><span class="delimiter">: </span><span class="description">test if two arguments are strictly equal.</span>
-   <span class="signature">[`isTruthy( value )`][@taktikorg/ipsum-aperiam/is-truthy]</span><span class="delimiter">: </span><span class="description">test if a value is truthy.</span>
-   <span class="signature">[`isUNCPath( value )`][@taktikorg/ipsum-aperiam/is-unc-path]</span><span class="delimiter">: </span><span class="description">test if a value is a UNC path.</span>
-   <span class="signature">[`isUndefinedOrNull( value )`][@taktikorg/ipsum-aperiam/is-undefined-or-null]</span><span class="delimiter">: </span><span class="description">test if a value is undefined or null.</span>
-   <span class="signature">[`isUppercase( value )`][@taktikorg/ipsum-aperiam/is-uppercase]</span><span class="delimiter">: </span><span class="description">test if a value is an uppercase string.</span>
-   <span class="signature">[`isURI( value )`][@taktikorg/ipsum-aperiam/is-uri]</span><span class="delimiter">: </span><span class="description">test if a value is a URI.</span>
-   <span class="signature">[`isWhitespace( value )`][@taktikorg/ipsum-aperiam/is-whitespace]</span><span class="delimiter">: </span><span class="description">test whether a string contains only white space characters.</span>
-   <span class="signature">[`isWritablePropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-writable-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is writable.</span>
-   <span class="signature">[`isWritableProperty( value, property )`][@taktikorg/ipsum-aperiam/is-writable-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is writable.</span>
-   <span class="signature">[`isWriteOnlyPropertyIn( value, property )`][@taktikorg/ipsum-aperiam/is-write-only-property-in]</span><span class="delimiter">: </span><span class="description">test if an object's own or inherited property is write-only.</span>
-   <span class="signature">[`isWriteOnlyProperty( value, property )`][@taktikorg/ipsum-aperiam/is-write-only-property]</span><span class="delimiter">: </span><span class="description">test if an object's own property is write-only.</span>
-   <span class="signature">[`tools`][@taktikorg/ipsum-aperiam/tools]</span><span class="delimiter">: </span><span class="description">assertion utility tools.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- TODO: better examples -->

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var assert = require( '@taktikorg/ipsum-aperiam' );

console.log( objectKeys( assert ) );
```

</section>

<!-- /.examples -->

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@taktikorg/ipsum-aperiam.svg
[npm-url]: https://npmjs.org/package/@taktikorg/ipsum-aperiam

[test-image]: https://github.com/taktikorg/ipsum-aperiam/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/taktikorg/ipsum-aperiam/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/taktikorg/ipsum-aperiam/main.svg
[coverage-url]: https://codecov.io/github/taktikorg/ipsum-aperiam?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/taktikorg/ipsum-aperiam.svg
[dependencies-url]: https://david-dm.org/taktikorg/ipsum-aperiam/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/taktikorg/ipsum-aperiam/tree/deno
[deno-readme]: https://github.com/taktikorg/ipsum-aperiam/blob/deno/README.md
[umd-url]: https://github.com/taktikorg/ipsum-aperiam/tree/umd
[umd-readme]: https://github.com/taktikorg/ipsum-aperiam/blob/umd/README.md
[esm-url]: https://github.com/taktikorg/ipsum-aperiam/tree/esm
[esm-readme]: https://github.com/taktikorg/ipsum-aperiam/blob/esm/README.md
[branches-url]: https://github.com/taktikorg/ipsum-aperiam/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/taktikorg/ipsum-aperiam/main/LICENSE

<!-- <toc-links> -->

[@taktikorg/ipsum-aperiam/contains]: https://github.com/taktikorg/ipsum-aperiam/tree/main/contains

[@taktikorg/ipsum-aperiam/deep-equal]: https://github.com/taktikorg/ipsum-aperiam/tree/main/deep-equal

[@taktikorg/ipsum-aperiam/deep-has-own-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/deep-has-own-property

[@taktikorg/ipsum-aperiam/deep-has-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/deep-has-property

[@taktikorg/ipsum-aperiam/has-own-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-own-property

[@taktikorg/ipsum-aperiam/has-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-property

[@taktikorg/ipsum-aperiam/has-utf16-surrogate-pair-at]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-utf16-surrogate-pair-at

[@taktikorg/ipsum-aperiam/instance-of]: https://github.com/taktikorg/ipsum-aperiam/tree/main/instance-of

[@taktikorg/ipsum-aperiam/is-absolute-http-uri]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-absolute-http-uri

[@taktikorg/ipsum-aperiam/is-absolute-path]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-absolute-path

[@taktikorg/ipsum-aperiam/is-absolute-uri]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-absolute-uri

[@taktikorg/ipsum-aperiam/is-accessor-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-accessor-property-in

[@taktikorg/ipsum-aperiam/is-accessor-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-accessor-property

[@taktikorg/ipsum-aperiam/is-alphagram]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-alphagram

[@taktikorg/ipsum-aperiam/is-alphanumeric]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-alphanumeric

[@taktikorg/ipsum-aperiam/is-anagram]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-anagram

[@taktikorg/ipsum-aperiam/is-arguments]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-arguments

[@taktikorg/ipsum-aperiam/is-arrow-function]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-arrow-function

[@taktikorg/ipsum-aperiam/is-ascii]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-ascii

[@taktikorg/ipsum-aperiam/is-between]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-between

[@taktikorg/ipsum-aperiam/is-bigint]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-bigint

[@taktikorg/ipsum-aperiam/is-binary-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-binary-string

[@taktikorg/ipsum-aperiam/is-blank-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-blank-string

[@taktikorg/ipsum-aperiam/is-boxed-primitive]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-boxed-primitive

[@taktikorg/ipsum-aperiam/is-buffer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-buffer

[@taktikorg/ipsum-aperiam/is-camelcase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-camelcase

[@taktikorg/ipsum-aperiam/is-capitalized]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-capitalized

[@taktikorg/ipsum-aperiam/is-circular]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-circular

[@taktikorg/ipsum-aperiam/is-class]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-class

[@taktikorg/ipsum-aperiam/is-collection]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-collection

[@taktikorg/ipsum-aperiam/is-composite]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-composite

[@taktikorg/ipsum-aperiam/is-configurable-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-configurable-property-in

[@taktikorg/ipsum-aperiam/is-configurable-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-configurable-property

[@taktikorg/ipsum-aperiam/is-constantcase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-constantcase

[@taktikorg/ipsum-aperiam/is-current-year]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-current-year

[@taktikorg/ipsum-aperiam/is-data-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-data-property-in

[@taktikorg/ipsum-aperiam/is-data-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-data-property

[@taktikorg/ipsum-aperiam/is-dataview]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-dataview

[@taktikorg/ipsum-aperiam/is-digit-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-digit-string

[@taktikorg/ipsum-aperiam/is-domain-name]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-domain-name

[@taktikorg/ipsum-aperiam/is-duration-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-duration-string

[@taktikorg/ipsum-aperiam/is-email-address]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-email-address

[@taktikorg/ipsum-aperiam/is-empty-collection]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-empty-collection

[@taktikorg/ipsum-aperiam/is-empty-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-empty-object

[@taktikorg/ipsum-aperiam/is-empty-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-empty-string

[@taktikorg/ipsum-aperiam/is-enumerable-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-enumerable-property-in

[@taktikorg/ipsum-aperiam/is-enumerable-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-enumerable-property

[@taktikorg/ipsum-aperiam/is-even]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-even

[@taktikorg/ipsum-aperiam/is-falsy]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-falsy

[@taktikorg/ipsum-aperiam/is-finite]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-finite

[@taktikorg/ipsum-aperiam/is-generator-object-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-generator-object-like

[@taktikorg/ipsum-aperiam/is-generator-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-generator-object

[@taktikorg/ipsum-aperiam/is-gzip-buffer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-gzip-buffer

[@taktikorg/ipsum-aperiam/is-hex-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-hex-string

[@taktikorg/ipsum-aperiam/is-infinite]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-infinite

[@taktikorg/ipsum-aperiam/is-inherited-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-inherited-property

[@taktikorg/ipsum-aperiam/is-iterable-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-iterable-like

[@taktikorg/ipsum-aperiam/is-iterator-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-iterator-like

[@taktikorg/ipsum-aperiam/is-json]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-json

[@taktikorg/ipsum-aperiam/is-kebabcase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-kebabcase

[@taktikorg/ipsum-aperiam/is-leap-year]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-leap-year

[@taktikorg/ipsum-aperiam/is-localhost]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-localhost

[@taktikorg/ipsum-aperiam/is-lowercase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-lowercase

[@taktikorg/ipsum-aperiam/is-method-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-method-in

[@taktikorg/ipsum-aperiam/is-method]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-method

[@taktikorg/ipsum-aperiam/is-multi-slice]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-multi-slice

[@taktikorg/ipsum-aperiam/is-named-typed-tuple-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-named-typed-tuple-like

[@taktikorg/ipsum-aperiam/is-native-function]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-native-function

[@taktikorg/ipsum-aperiam/is-negative-zero]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-negative-zero

[@taktikorg/ipsum-aperiam/is-node-builtin]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-builtin

[@taktikorg/ipsum-aperiam/is-node-duplex-stream-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-duplex-stream-like

[@taktikorg/ipsum-aperiam/is-node-readable-stream-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-readable-stream-like

[@taktikorg/ipsum-aperiam/is-node-repl]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-repl

[@taktikorg/ipsum-aperiam/is-node-stream-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-stream-like

[@taktikorg/ipsum-aperiam/is-node-transform-stream-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-transform-stream-like

[@taktikorg/ipsum-aperiam/is-node-writable-stream-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node-writable-stream-like

[@taktikorg/ipsum-aperiam/is-nonconfigurable-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonconfigurable-property-in

[@taktikorg/ipsum-aperiam/is-nonconfigurable-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonconfigurable-property

[@taktikorg/ipsum-aperiam/is-nonenumerable-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonenumerable-property-in

[@taktikorg/ipsum-aperiam/is-nonenumerable-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonenumerable-property

[@taktikorg/ipsum-aperiam/is-nonnegative-finite]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonnegative-finite

[@taktikorg/ipsum-aperiam/is-object-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-object-like

[@taktikorg/ipsum-aperiam/is-odd]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-odd

[@taktikorg/ipsum-aperiam/is-pascalcase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-pascalcase

[@taktikorg/ipsum-aperiam/is-plain-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-plain-object

[@taktikorg/ipsum-aperiam/is-positive-zero]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-positive-zero

[@taktikorg/ipsum-aperiam/is-prime]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-prime

[@taktikorg/ipsum-aperiam/is-primitive]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-primitive

[@taktikorg/ipsum-aperiam/is-prng-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-prng-like

[@taktikorg/ipsum-aperiam/is-probability]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-probability

[@taktikorg/ipsum-aperiam/is-property-key]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-property-key

[@taktikorg/ipsum-aperiam/is-prototype-of]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-prototype-of

[@taktikorg/ipsum-aperiam/is-read-only-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-read-only-property-in

[@taktikorg/ipsum-aperiam/is-read-only-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-read-only-property

[@taktikorg/ipsum-aperiam/is-read-write-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-read-write-property-in

[@taktikorg/ipsum-aperiam/is-read-write-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-read-write-property

[@taktikorg/ipsum-aperiam/is-readable-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-readable-property-in

[@taktikorg/ipsum-aperiam/is-readable-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-readable-property

[@taktikorg/ipsum-aperiam/is-regexp-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-regexp-string

[@taktikorg/ipsum-aperiam/is-relative-path]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-relative-path

[@taktikorg/ipsum-aperiam/is-relative-uri]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-relative-uri

[@taktikorg/ipsum-aperiam/is-same-complex128]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-complex128

[@taktikorg/ipsum-aperiam/is-same-complex64]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-complex64

[@taktikorg/ipsum-aperiam/is-same-native-class]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-native-class

[@taktikorg/ipsum-aperiam/is-same-type]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-type

[@taktikorg/ipsum-aperiam/is-same-value-zero]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-value-zero

[@taktikorg/ipsum-aperiam/is-same-value]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-value

[@taktikorg/ipsum-aperiam/is-semver]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-semver

[@taktikorg/ipsum-aperiam/is-slice]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-slice

[@taktikorg/ipsum-aperiam/is-snakecase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-snakecase

[@taktikorg/ipsum-aperiam/is-startcase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-startcase

[@taktikorg/ipsum-aperiam/is-strict-equal]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-strict-equal

[@taktikorg/ipsum-aperiam/is-truthy]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-truthy

[@taktikorg/ipsum-aperiam/is-unc-path]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-unc-path

[@taktikorg/ipsum-aperiam/is-undefined-or-null]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-undefined-or-null

[@taktikorg/ipsum-aperiam/is-uppercase]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uppercase

[@taktikorg/ipsum-aperiam/is-uri]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uri

[@taktikorg/ipsum-aperiam/is-whitespace]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-whitespace

[@taktikorg/ipsum-aperiam/is-writable-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-writable-property-in

[@taktikorg/ipsum-aperiam/is-writable-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-writable-property

[@taktikorg/ipsum-aperiam/is-write-only-property-in]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-write-only-property-in

[@taktikorg/ipsum-aperiam/is-write-only-property]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-write-only-property

[@taktikorg/ipsum-aperiam/tools]: https://github.com/taktikorg/ipsum-aperiam/tree/main/tools

[@taktikorg/ipsum-aperiam/has-arraybuffer-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-arraybuffer-support

[@taktikorg/ipsum-aperiam/has-arrow-function-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-arrow-function-support

[@taktikorg/ipsum-aperiam/has-async-await-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-async-await-support

[@taktikorg/ipsum-aperiam/has-async-iterator-symbol-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-async-iterator-symbol-support

[@taktikorg/ipsum-aperiam/has-bigint-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-bigint-support

[@taktikorg/ipsum-aperiam/has-bigint64array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-bigint64array-support

[@taktikorg/ipsum-aperiam/has-biguint64array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-biguint64array-support

[@taktikorg/ipsum-aperiam/has-class-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-class-support

[@taktikorg/ipsum-aperiam/has-dataview-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-dataview-support

[@taktikorg/ipsum-aperiam/has-define-properties-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-define-properties-support

[@taktikorg/ipsum-aperiam/has-define-property-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-define-property-support

[@taktikorg/ipsum-aperiam/has-float32array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-float32array-support

[@taktikorg/ipsum-aperiam/has-float64array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-float64array-support

[@taktikorg/ipsum-aperiam/has-function-name-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-function-name-support

[@taktikorg/ipsum-aperiam/has-generator-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-generator-support

[@taktikorg/ipsum-aperiam/has-globalthis-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-globalthis-support

[@taktikorg/ipsum-aperiam/has-int16array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-int16array-support

[@taktikorg/ipsum-aperiam/has-int32array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-int32array-support

[@taktikorg/ipsum-aperiam/has-int8array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-int8array-support

[@taktikorg/ipsum-aperiam/has-iterator-symbol-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-iterator-symbol-support

[@taktikorg/ipsum-aperiam/has-map-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-map-support

[@taktikorg/ipsum-aperiam/has-node-buffer-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-node-buffer-support

[@taktikorg/ipsum-aperiam/has-proxy-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-proxy-support

[@taktikorg/ipsum-aperiam/has-set-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-set-support

[@taktikorg/ipsum-aperiam/has-sharedarraybuffer-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-sharedarraybuffer-support

[@taktikorg/ipsum-aperiam/has-symbol-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-symbol-support

[@taktikorg/ipsum-aperiam/has-tostringtag-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-tostringtag-support

[@taktikorg/ipsum-aperiam/has-uint16array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-uint16array-support

[@taktikorg/ipsum-aperiam/has-uint32array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-uint32array-support

[@taktikorg/ipsum-aperiam/has-uint8array-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-uint8array-support

[@taktikorg/ipsum-aperiam/has-uint8clampedarray-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-uint8clampedarray-support

[@taktikorg/ipsum-aperiam/has-wasm-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-wasm-support

[@taktikorg/ipsum-aperiam/has-weakmap-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-weakmap-support

[@taktikorg/ipsum-aperiam/has-weakset-support]: https://github.com/taktikorg/ipsum-aperiam/tree/main/has-weakset-support

[@taktikorg/ipsum-aperiam/is-big-endian]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-big-endian

[@taktikorg/ipsum-aperiam/is-browser]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-browser

[@taktikorg/ipsum-aperiam/is-darwin]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-darwin

[@taktikorg/ipsum-aperiam/is-docker]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-docker

[@taktikorg/ipsum-aperiam/is-electron-main]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-electron-main

[@taktikorg/ipsum-aperiam/is-electron-renderer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-electron-renderer

[@taktikorg/ipsum-aperiam/is-electron]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-electron

[@taktikorg/ipsum-aperiam/is-little-endian]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-little-endian

[@taktikorg/ipsum-aperiam/is-mobile]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-mobile

[@taktikorg/ipsum-aperiam/is-node]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-node

[@taktikorg/ipsum-aperiam/is-touch-device]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-touch-device

[@taktikorg/ipsum-aperiam/is-web-worker]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-web-worker

[@taktikorg/ipsum-aperiam/is-windows]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-windows

[@taktikorg/ipsum-aperiam/is-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-error

[@taktikorg/ipsum-aperiam/is-eval-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-eval-error

[@taktikorg/ipsum-aperiam/is-range-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-range-error

[@taktikorg/ipsum-aperiam/is-reference-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-reference-error

[@taktikorg/ipsum-aperiam/is-syntax-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-syntax-error

[@taktikorg/ipsum-aperiam/is-type-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-type-error

[@taktikorg/ipsum-aperiam/is-uri-error]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uri-error

[@taktikorg/ipsum-aperiam/is-accessor-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-accessor-array

[@taktikorg/ipsum-aperiam/is-array-length]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-array-length

[@taktikorg/ipsum-aperiam/is-array-like-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-array-like-object

[@taktikorg/ipsum-aperiam/is-array-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-array-like

[@taktikorg/ipsum-aperiam/is-arraybuffer-view]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-arraybuffer-view

[@taktikorg/ipsum-aperiam/is-arraybuffer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-arraybuffer

[@taktikorg/ipsum-aperiam/is-between-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-between-array

[@taktikorg/ipsum-aperiam/is-bigint64array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-bigint64array

[@taktikorg/ipsum-aperiam/is-biguint64array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-biguint64array

[@taktikorg/ipsum-aperiam/is-circular-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-circular-array

[@taktikorg/ipsum-aperiam/is-empty-array-like-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-empty-array-like-object

[@taktikorg/ipsum-aperiam/is-empty-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-empty-array

[@taktikorg/ipsum-aperiam/is-falsy-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-falsy-array

[@taktikorg/ipsum-aperiam/is-finite-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-finite-array

[@taktikorg/ipsum-aperiam/is-numeric-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-numeric-array

[@taktikorg/ipsum-aperiam/is-plain-object-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-plain-object-array

[@taktikorg/ipsum-aperiam/is-probability-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-probability-array

[@taktikorg/ipsum-aperiam/is-same-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-array

[@taktikorg/ipsum-aperiam/is-same-complex128array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-complex128array

[@taktikorg/ipsum-aperiam/is-same-complex64array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-complex64array

[@taktikorg/ipsum-aperiam/is-same-float32array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-float32array

[@taktikorg/ipsum-aperiam/is-same-float64array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-same-float64array

[@taktikorg/ipsum-aperiam/is-sharedarraybuffer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-sharedarraybuffer

[@taktikorg/ipsum-aperiam/is-truthy-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-truthy-array

[@taktikorg/ipsum-aperiam/is-typed-array-length]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-typed-array-length

[@taktikorg/ipsum-aperiam/is-typed-array-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-typed-array-like

[@taktikorg/ipsum-aperiam/is-typed-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-typed-array

[@taktikorg/ipsum-aperiam/is-unity-probability-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-unity-probability-array

[@taktikorg/ipsum-aperiam/is-complex-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex-like

[@taktikorg/ipsum-aperiam/is-complex-typed-array-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex-typed-array-like

[@taktikorg/ipsum-aperiam/is-complex-typed-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex-typed-array

[@taktikorg/ipsum-aperiam/is-complex]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex

[@taktikorg/ipsum-aperiam/is-complex128]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex128

[@taktikorg/ipsum-aperiam/is-complex128array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex128array

[@taktikorg/ipsum-aperiam/is-complex64]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex64

[@taktikorg/ipsum-aperiam/is-complex64array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex64array

[@taktikorg/ipsum-aperiam/is-centrosymmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-centrosymmetric-matrix

[@taktikorg/ipsum-aperiam/is-complex128matrix-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex128matrix-like

[@taktikorg/ipsum-aperiam/is-complex128ndarray-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex128ndarray-like

[@taktikorg/ipsum-aperiam/is-complex128vector-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex128vector-like

[@taktikorg/ipsum-aperiam/is-complex64matrix-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex64matrix-like

[@taktikorg/ipsum-aperiam/is-complex64ndarray-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex64ndarray-like

[@taktikorg/ipsum-aperiam/is-complex64vector-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-complex64vector-like

[@taktikorg/ipsum-aperiam/is-float32matrix-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float32matrix-like

[@taktikorg/ipsum-aperiam/is-float32ndarray-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float32ndarray-like

[@taktikorg/ipsum-aperiam/is-float32vector-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float32vector-like

[@taktikorg/ipsum-aperiam/is-float64matrix-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float64matrix-like

[@taktikorg/ipsum-aperiam/is-float64ndarray-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float64ndarray-like

[@taktikorg/ipsum-aperiam/is-float64vector-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float64vector-like

[@taktikorg/ipsum-aperiam/is-matrix-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-matrix-like

[@taktikorg/ipsum-aperiam/is-ndarray-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-ndarray-like

[@taktikorg/ipsum-aperiam/is-nonsymmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonsymmetric-matrix

[@taktikorg/ipsum-aperiam/is-persymmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-persymmetric-matrix

[@taktikorg/ipsum-aperiam/is-skew-centrosymmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-skew-centrosymmetric-matrix

[@taktikorg/ipsum-aperiam/is-skew-persymmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-skew-persymmetric-matrix

[@taktikorg/ipsum-aperiam/is-skew-symmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-skew-symmetric-matrix

[@taktikorg/ipsum-aperiam/is-square-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-square-matrix

[@taktikorg/ipsum-aperiam/is-symmetric-matrix]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-symmetric-matrix

[@taktikorg/ipsum-aperiam/is-vector-like]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-vector-like

[@taktikorg/ipsum-aperiam/is-float32array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float32array

[@taktikorg/ipsum-aperiam/is-float64array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-float64array

[@taktikorg/ipsum-aperiam/is-int16array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-int16array

[@taktikorg/ipsum-aperiam/is-int32array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-int32array

[@taktikorg/ipsum-aperiam/is-int8array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-int8array

[@taktikorg/ipsum-aperiam/is-uint16array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uint16array

[@taktikorg/ipsum-aperiam/is-uint32array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uint32array

[@taktikorg/ipsum-aperiam/is-uint8array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uint8array

[@taktikorg/ipsum-aperiam/is-uint8clampedarray]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-uint8clampedarray

[@taktikorg/ipsum-aperiam/is-cube-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-cube-number

[@taktikorg/ipsum-aperiam/is-integer-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-integer-array

[@taktikorg/ipsum-aperiam/is-integer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-integer

[@taktikorg/ipsum-aperiam/is-negative-integer-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-negative-integer-array

[@taktikorg/ipsum-aperiam/is-negative-integer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-negative-integer

[@taktikorg/ipsum-aperiam/is-negative-number-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-negative-number-array

[@taktikorg/ipsum-aperiam/is-negative-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-negative-number

[@taktikorg/ipsum-aperiam/is-nonnegative-integer-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonnegative-integer-array

[@taktikorg/ipsum-aperiam/is-nonnegative-integer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonnegative-integer

[@taktikorg/ipsum-aperiam/is-nonnegative-number-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonnegative-number-array

[@taktikorg/ipsum-aperiam/is-nonnegative-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonnegative-number

[@taktikorg/ipsum-aperiam/is-nonpositive-integer-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonpositive-integer-array

[@taktikorg/ipsum-aperiam/is-nonpositive-integer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonpositive-integer

[@taktikorg/ipsum-aperiam/is-nonpositive-number-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonpositive-number-array

[@taktikorg/ipsum-aperiam/is-nonpositive-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nonpositive-number

[@taktikorg/ipsum-aperiam/is-positive-integer-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-positive-integer-array

[@taktikorg/ipsum-aperiam/is-positive-integer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-positive-integer

[@taktikorg/ipsum-aperiam/is-positive-number-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-positive-number-array

[@taktikorg/ipsum-aperiam/is-positive-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-positive-number

[@taktikorg/ipsum-aperiam/is-safe-integer-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-safe-integer-array

[@taktikorg/ipsum-aperiam/is-safe-integer]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-safe-integer

[@taktikorg/ipsum-aperiam/is-square-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-square-number

[@taktikorg/ipsum-aperiam/is-square-triangular-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-square-triangular-number

[@taktikorg/ipsum-aperiam/is-triangular-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-triangular-number

[@taktikorg/ipsum-aperiam/is-array-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-array-array

[@taktikorg/ipsum-aperiam/is-boolean-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-boolean-array

[@taktikorg/ipsum-aperiam/is-date-object-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-date-object-array

[@taktikorg/ipsum-aperiam/is-function-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-function-array

[@taktikorg/ipsum-aperiam/is-nan-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nan-array

[@taktikorg/ipsum-aperiam/is-null-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-null-array

[@taktikorg/ipsum-aperiam/is-number-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-number-array

[@taktikorg/ipsum-aperiam/is-object-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-object-array

[@taktikorg/ipsum-aperiam/is-string-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-string-array

[@taktikorg/ipsum-aperiam/is-symbol-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-symbol-array

[@taktikorg/ipsum-aperiam/is-array]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-array

[@taktikorg/ipsum-aperiam/is-boolean]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-boolean

[@taktikorg/ipsum-aperiam/is-date-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-date-object

[@taktikorg/ipsum-aperiam/is-function]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-function

[@taktikorg/ipsum-aperiam/is-nan]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-nan

[@taktikorg/ipsum-aperiam/is-null]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-null

[@taktikorg/ipsum-aperiam/is-number]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-number

[@taktikorg/ipsum-aperiam/is-object]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-object

[@taktikorg/ipsum-aperiam/is-regexp]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-regexp

[@taktikorg/ipsum-aperiam/is-string]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-string

[@taktikorg/ipsum-aperiam/is-symbol]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-symbol

[@taktikorg/ipsum-aperiam/is-undefined]: https://github.com/taktikorg/ipsum-aperiam/tree/main/is-undefined

<!-- </toc-links> -->

</section>

<!-- /.links -->
