# _Aurror
Gradient mixin' library

* Required SASS runnin' for use.
* Currently works only on Chrome 10+


This _Aurror auto generates good lookin' gradient with a single line of SASS.
Is recommended to run 'sass --watch assets/scss:assets' from _Aurror root directory.

Available in latest version library:

## aurrorIt()
####aurrorIt generates gradient light to dark from selected color, 


Syntax is as follows:

.css-selector {
	@include aurrorIt( $gradient-direction, $color-start )
}


* $gradient-direction = top | left | bottom | right
* $color-start = hex | rgb | rgba | hsl | hsla
 

2. aurrorItCompl()
While ####aurrorIt()##### generates from light to dark, ####aurrorItCompl#### generates complimentary color for color-stop from given color.

Syntax is as follows:

.css-selector {
	@include aurrorItCompl( $gradient-direction, $hue-start, $color-type )
}


* $gradient-direction = top | left | bottom | right
* $hue-start =  red 0 to red 360, will work just fine for hue > 360 e.g. 1000
* $color-type = pastel | gothic
