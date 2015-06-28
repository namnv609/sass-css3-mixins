# SASS CSS3 Mixins
This repository is simple add vendor prefix for CSS3 properties.

By default, vendor prefix list support ``-webkit-``, ``-moz-``, ``-o-``, ``-khtml-``, ``-ms-`` and W3C. You can override vendor list by re-defined ``$vendorPrefixes`` variable. Or you can add new CSS3 property by using mixin css3-prefix and css3-function

SASS example:
```
@import "css3-mixins"
$vendorPrefixes: (-webkit-, -moz-, -o-)

body
    .box
        +border-radius(5px)
        +box-shadow(2px 2px 2px #CCC inset)
```

SCSS example:
```
@import "css3-mixins";
$vendorPrefixes: (-webkit-, -moz-, -o-);

body {
    .box {
        @include border-radius(5px);
        @include box-shadow(2px 2px 2px #CCC inset);
    }
}
```

* css3-prefix
    * SASS
    ```
    +css3-prefix(propertyName, listValue)
    ```
    * SCSS
    ```
    @include css3-prefix(propertyName, listValue);
    ```
* css3-function
    * SASS
    ```
    +css3-function(propertyName, css3FunctionName, listValue)
    ```
    * SCSS
    ```
    @include css3-function(propertyName, css3FunctionName, listValue);
    ```
## List CSS3 properties
* Border radius
    * border-radius
    * border-top-left-radius
    * border-top-right-radius
    * border-bottom-left-radius
    * border-bottom-right-radius
* Border image
    * border-image
    * border-image-outset
    * border-image-repeat
    * border-image-source
    * border-image-slice
    * border-image-width
* Multi-column properties
    * break-after
    * break-before
    * break-inside
    * columns
    * column-count
    * column-fill
    * column-gap
    * column-rule
    * column-rule-color
    * column-rule-style
    * column-rule-width
    * column-span
    * column-width
* Animation properties
    * @keyframes
    * animation
    * animation-delay
    * amination-direction
    * animation-duration
    * animation-fill-mode
    * animation-iteration-count
    * animation-name
    * animation-play-state
    * animation-timing-function
* Transition properties
    * transition
    * transition-delay
    * transition-duration
    * transition-timing-function
    * transition-property
* Transform properties
    * backface-visibility
    * perspective
    * perspective-origin
    * transform
    * transform-origin
    * transform-style
* New background properties
    * background-clip
    * background-origin
    * background-size
* Color gradients
    * Linear gradients
    * Radial gradients
* Others new properties
    * appearance
    * box-shadow
    * box-decoration-break
    * opacity
