---
layout: default
---

<!-- Note: This file is automatically generated from source code comments. Changes made in this file will be overridden. -->

<h1 id="function-rotationmatrix">Function rotationMatrix <a href="#function-rotationmatrix" title="Permalink">#</a></h1>

Create a 2-dimensional counter-clockwise rotation matrix (2x2) for a given angle (expressed in radians).
Create a 2-dimensional counter-clockwise rotation matrix (3x3) by a given angle (expressed in radians) around a given axis (1x3).


<h2 id="syntax">Syntax <a href="#syntax" title="Permalink">#</a></h2>

```js
math.rotationMatrix(theta)
math.rotationMatrix(theta, format)
math.rotationMatrix(theta, [v])
math.rotationMatrix(theta, [v], format)
```

<h3 id="parameters">Parameters <a href="#parameters" title="Permalink">#</a></h3>

Parameter | Type | Description
--------- | ---- | -----------
`theta` | number &#124; BigNumber &#124; Complex &#124; Unit | Rotation angle
`v` | Array &#124; Matrix | Rotation axis
`format` | string | Result Matrix storage format

<h3 id="returns">Returns <a href="#returns" title="Permalink">#</a></h3>

Type | Description
---- | -----------
Array &#124; Matrix | Rotation matrix


<h2 id="examples">Examples <a href="#examples" title="Permalink">#</a></h2>

```js
math.rotationMatrix(math.pi / 2)                      // returns [[0, -1], [1, 0]]
math.rotationMatrix(math.bignumber(45))               // returns [[ bignumber(1 / sqrt(2)), - bignumber(1 / sqrt(2))], [ bignumber(1 / sqrt(2)),  bignumber(1 / sqrt(2))]]
math.rotationMatrix(math.complex(1 + i))              // returns [[cos(1 + i), -sin(1 + i)], [sin(1 + i), cos(1 + i)]]
math.rotationMatrix(math.unit('1rad'))                // returns [[cos(1), -sin(1)], [sin(1), cos(1)]]

math.rotationMatrix(math.pi / 2, [0, 1, 0])           // returns [[0, 0, 1], [0, 1, 0], [-1, 0, 0]]
math.rotationMatrix(math.pi / 2, matrix([0, 1, 0]))   // returns matrix([[0, 0, 1], [0, 1, 0], [-1, 0, 0]])

```


<h2 id="see-also">See also <a href="#see-also" title="Permalink">#</a></h2>

[matrix](matrix.html),
[cos](cos.html),
[sin](sin.html)