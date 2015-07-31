# _Aurror
Gradient mixin' library

## Lines of infinity in a single line
It has come to my concern that many developers have problem to find perfect color for gradients, and many designers have problems in coding. This _Aurror lets them create gradients in seconds while keeping colors seamless and coding dry.

* Required SASS runnin' for use.
* Currently works only on Chrome 10+


This _Aurror auto generates good lookin' gradient with a single line of SASS.
Is recommended to run sass --watch assets/scss:asset from _Aurror root directory.

Available in latest version library:

## aurrorItMonochromatic()
aurrorItMonochromatic generates gradient light to dark/dark to light from selected color, 


Syntax is as follows:

.css-selector {
	@include aurrorItMonochromatic( $gradient-direction, $color-start, $lightness );
}


* $gradient-direction = top | left | bottom | right
* $color-start = hex | rgb | rgba | hsl | hsla
* $lightness = darker | lighter 


## aurrorItComplementary()
While aurrorItMonochromatic() generates darker/lighter color,
aurrorItComplementary() generates complimentary (opposite) color for color-stop from given color.

Syntax is as follows:

.css-selector {
	@include aurrorItComplementary( $gradient-direction, $hue-start, $color-type, $alpha-start, $alpha-end );
}


* $gradient-direction = top | left | bottom | right
* $hue-start =  between 0 to 360, will work just fine for hue > 360 e.g. 1000
* $color-type = pastel | gothic | pale
* $alpha-start = starting opacity which the gradient starts
* $alpha-end = starting opacity which the gradient end

## aurrorItAnalogous()
This mixin generates gradient of colors located adjacent (next to) to each other on color wheel.

Syntax:
.css-selector {
	@include aurrorItAnalogous( $gradient-direction, $hue-start, $hue-direction, $alpha-start, $alpha-end );
}
* $gradient-direction = top | left | bottom | right
* $hue-start =  between 0 to 360, will work just fine for hue > 360 e.g. 1000
* $hue-direction = left | right
* $alpha-start = starting opacity which the gradient starts
* $alpha-end = starting opacity which the gradient end

### added
Socials logo color library = _Aurror/assets/scss/variables/_logocolors.scss
