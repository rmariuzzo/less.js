less.js + blending modes
========================

The **dynamic** stylesheet language, powered with blending modes.

The full credits for the original project of LESS goes to Alexis Sellier, more information: <http://lesscss.org>.

about
-----

This is the JavaScript stable version of LESS with some blending modes (such those from Photoshop, GIMP or Fireworks).

These blending methods are implemented as LESS operations.

blending modes
--------------

**list of implemented blending modes**

 * multiply
 * screen
 * overlay
 * softlight
 * hardlight
 * difference
 * exclusion
 * average
 * negation

documentation
-------------

###multiply
Multiply two colors. For each two colors their RGB channel are multiplied then divided by 255. The result is a darker color.

Parameters:

* `color1`: A color object to multiply against.
* `color2`: A color object to multiply against.

Returns: `color`

Example:

    multiply(#ff6600, #000000);

###screen
Do the opposite effect from `multiply`. The result is a brighter color.

Parameters:

* `color1`: A color object to _screen_ against.
* `color2`: A color object to _screen_ against.

Returns: `color`

Example:

    screen(#ff6600, #000000);

###overlay
Combines the effect from both `multiply` and `screen`. Conditionally make light channels lighter and dark channels darker. **Note**: The results of the conditions are determined by the first color parameter.

Parameters:

* `color1`: A color object to overlay another. Also it is the determinant color to make the result lighter or darker.
* `color2`: A color object to be _overlayed_.

Returns: `color`

Example:

    overlay(#ff6600, #000000);

###softlight
Similar to `overlay` but avoid pure black resulting in pure black, and pure white resulting in pure white.

Parameters:

* `color1`: A color object to _soft light_ another.
* `color2`: A color object to be _soft lighten_.

Returns: `color`

Example:

    softlight(#ff6600, #000000);

###hardlight
Similar to `overlay` but use the second color to detect light and dark channels instead of using the first color.

Parameters:

* `color1`: A color object to overlay another.
* `color2`: A color object to be _overlayed_. Also it is the determinant color to make the result lighter or darker.

Returns: `color`

Example:

    overlay(#ff6600, #000000);

###difference
Substracts the second color from the first color. The operation is made per RGB channels. The result is a darker color.

Parameters:

* `color1`: A color object to act as the minuend.
* `color2`: A color object to act as the subtrahend.

Returns: `color`

Example:

    difference(#ff6600, #000000);

###exclusion
Similar effect to `difference` with lower contrast.

Parameters:

* `color1`: A color object to act as the minuend.
* `color2`: A color object to act as the subtrahend.

Returns: `color`

Example:

    exclusion(#ff6600, #000000);

###average
Compute the average of two colors. The operation is made per RGB channels.

Parameters:

* `color1`: A color object.
* `color2`: A color object.

Returns: `color`

Example:

    average(#ff6600, #000000);

###negation
Do the opposite effect from `difference`. The result is a brighter color. **Note**: The _opposite_ effect doesn't mean the _inverted_ effect as resulting to an _addition_ operation.

Parameters:

* `color1`: A color object to act as the minuend.
* `color2`: A color object to act as the subtrahend.

Returns: `color`

Example:

    negation(#ff6600, #000000);


license
-------

See `LICENSE` file.

> Copyright (c) 2012 Rubens Mariuzzo
