#Tatami CSS
Tatami is a beautiful, fully responsive, style agnostic CSS boilerplate written in LESS.

It is based on other similar projects as [Skeleton](getskeleton.com), [Preboot](getpreboot.com) and [Boostrap](twitter.github.io/bootstrap/‎). It includes:

* a flexible CSS grid;
* a base stylesheet;
* a set of useful LESS mixins.

##Flexible CSS Grid
Tatami includes LESS mixins to obtain fluid and fixed grids.

`#grid > .base-classes()` prints grids base classes.

`#grid > .grid(@width, @pxGutterWitdh, @numberOfColumns)` prints fixed grid specific classes.

`#grid > .grid(@maxWidth, @%gutterWidth, @numberOfColumns)` prints fluid grid specific classes.

`#grid > .mobile(@pxGutterWitdh)` prints specific classes for mobile devices.

####Usage Example

```less
\#grid > .base-classes();

\#grid > .grid(1170px, 30px, 12);

\#grid > .grid(percentage(1), percentage(0.02564102564103), 12);

@media only screen and (min-width: 980px) and (max-width: 1169px) {
	#grid > .grid(980px, 24px, 12);
}

@media only screen and (min-width: 768px) and (max-width: 979px) {
	#grid > .grid(768px, 20px, 12);
}

@media only screen and (max-width: 767px) {
	#grid > .mobile(15px);
}
```

##Base stylesheet
Check the files into the expamles folder.

Tatami defines a set of variables which guide the aspect defined in the base stylesheet.

```Less
//Controls root font size
@fontSize: 14px;

//Controls root base line and element margins
@baselineSize: 20px;

//Controls the ul margin-left, the blockquote margin-left and border and all the other lateral spacing
@lateralSize: 30px;

//background color
@backgroundColor: #fff;

//root text color
@textColor: #444;

//hr and blockquote border colors 
@bordersColor: darken(spin(@textColor, 5), 10%);
@formsBorderColor: lighten(spin(@textColor, -10), 20%);
@formsFocusBorderColor: darken(spin(@textColor, 10), 20%);

//titles color
@titlesColor: darken(spin(@textColor, 5), 10%);

//link and link:hover colors
@linkColor: @textColor;
@linkHoverColor: arken(spin(@textColor, 5), 10%);

//button colors
@buttonColor: #ccc;
@buttonHoverColor: #aaa;

//base font stack and titles font stack
@baseFontStack: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
@titlesFontStack: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
```

##LESS Mixins

####Generic Mixins

`.clearfix()` a micro clearfix mixin;

`.center-block()`;

`.size(@width, @height)`;

`.square(@size)`;

`.resizable(@direction)`;

`.hide-text()` an image replacement mixin;

`.text-truncate()` a text overflow management mixin;

`.content-columns(@width, @count, @gap)` a CSS3 columns mixin;

`.opacity(@opacity)`

`.input-block-level()` a mixin to full-width input elements;

`.appearance(@string)`;

`.retina-image(@file-1x, @file-2x, @width-1x, @height-1x)`;

`placeholder(@color)`;

`user-select(@select)`;

`background-clip(@type)`;

`box-sizing (@type)`;

####Border Radius Mixins

`border-radius(@topright, @bottomright , @bottomleft , @topleft)`;

`border-radius(@radius)`;

`border-top-radius(@radius)`;

`border-right-radius(@radius)`;

`border-bottom-radius(@radius)`;

`border-left-radius(@radius)`;

####Shadow Mixins

`text-shadow(@string)`;

`drop-shadow(@string)`;

`inset-shadow(@string) `;

####Gradient Mixins

```less
\#gradient {
	.horizontal(@startColor, @endColor)

	.vertical(@startColor, @endColor)

	.directional(@startColor, @endColor, @deg) 

	.horizontal-three-colors(@startColor, @midColor, @colorStop, @endColor)

	.vertical-three-colors(@startColor, @midColor, @colorStop, @endColor)

	.radial(@innerColor, @outerColor)

	.striped(@color, @angle)
}
```

####IE Mixins

`reset-filter()` a mixin to reset IE filters;

####CSS Animations Mixins

`transition(@transition)`

`transition-property(@transition-property)`

`transition-duration(@transition-duration)`

`transition-delay(@transition-delay)`

`transition-duration(@transition-duration)`

`rotate(@degrees)`

`scale(@ratio)`

`translate(@x, @y)`

`skew(@x, @y)`

`translate3d(@x, @y, @z)`

`backface-visibility(@visibility)`

####Button Style Mixin

`buttonStyle (@baseColor, @hoverColor, @textColor, @borderColor)`