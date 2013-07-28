SASS-Multi-Box-Shadow
=====================

A SASS mixin for rendering box-shadows on multiple sides.

Requirements
------------
The multi-box-shadow assumes a 'box-shadow' mixin exists so Compass is required.

Documentation
------------
The multi-box-shadow mixin takes two arguments, both of which take variable argument lengths.
```sass
@include multi-box-shadow(shadow-sides, box-shadow-parameters);
```

The first argument, 'shadow-sides', has exactly the same format as the 'margin' CSS property.
Here, you specify the size of the shadow on each of the four sides.  You can use shorthand properties here.

The second argument, 'box-shadow-parameters', takes exactly the same arguments as a standard box-shadow without
the first two (horizontal and vertical) properties.

Example
------------
Let's say you use the box-shadow mixin to define a top shadow like this:
```sass
@include box-shadow(0 -10px 10px -10px $f00);
```

With the multi-box-shadow mixin you can easily make this top shadow appear on the left and right sides as well:
```sass
@include multi-box-shadow(10px 10px 0 10px, 10px -10px $f00);
```
