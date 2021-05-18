This repository contains HTML and CSS learning stuff.
==========================================================
------
My CSS Notes:-
----
CSS Selectors: A CSS selector selects the HTML element(s) you want to
style. We can divide CSS selectors into five categories:

1.Simple selectors (select elements based on name, id, class):
a)element-selector, ie, p b)id (\#), ie, \#id-name c)class (.), ie,
.container d)universal selector(*), ie, *

2.Combinator selectors (select elements based on a specific relationship
between them) a)descendant selector (space), ie, div p ,-\> selects all
the p which are child(decendants) of div b)child selector (\>) ie, div
\> p ,-\> selects p which are only direct child of div c)adjacent
sibling selector (+) ie, div + p ,-\> selects p which comes direct after
div ends(adjacent sibling) d)general sibling selector (\~) ie, div \~ p
,-\> selects all p which comes direct after div ends (general sibling)
e)grouping Selector ie, h1, p, .container -\> apply property to multiple
selector

3.Pseudo-class selectors (select elements based on a certain state) ,
ie, a:link, p:hover 4.Pseudo-elements selectors (select and style a part
of an element), ie, div::after, p:first-line, p::selection 5.Attribute
selectors [attribute] (select elements based on an attribute or
attribute value) -\> ie, input[type="text"],
a[href="https://google.com"],

All CSS Attribute Selectors Selector Example Example description
[attribute] [target] Selects all elements with a target attribute
[attribute=value] [target=\_blank] Selects all elements with
target="\_blank" [attribute\~=value] [title\~=flower] Selects all
elements with a title attribute containing the word "flower"
[attribute|=value] [lang|=en] Selects all elements with a lang attribute
value starting with "en" [attribute\^=value] a[href\^="https"] Selects
every <a> element whose href attribute value begins with "https"
[attribute\$=value] a[href\$=".pdf"] Selects every <a> element whose
href attribute value ends with ".pdf" [attribute\*=value]
a[href\*="hello"] Selects every <a> element whose href attribute value
contains the substring "hello"

=================================================================================================================================

Inline css has more priority (!important is exception) Then internal and
external whichever is written last. (!important is exception)

Selector priority order (!important is exception): 1.id 2.class
3.element 4.universal selector

================================================================================================================================

Background Properties:-
------------------------
background-color: (color, transparent) background-image: (url,
gradients, none) background-repeat: (repeat, no-repeat, repeat-x,
repeat-y) background-position: (top left | top center | top right |
center left | center center | center right | bottom left | bottom center
| bottom right

                    x-% y-%
                    x-px y-px)

background-attachment: (fixed, scroll, local) background-size: (auto,
cover, contain, %, px) background-origin: (border-box, padding-box,
content-box)
------------------------------------------------------------------------------------
The CSS background-origin property specifies where the background image
is positioned.

border-box - the background image starts from the upper left corner of
the border padding-box - (default) the background image starts from the
upper left corner of the padding edge content-box - the background image
starts from the upper left corner of the content
------------------------------------------------------------------------------------

background-clip: (border-box, padding-box, content-box);

The CSS background-clip property specifies the painting area of the
background. border-box - (default) the background is painted to the
outside edge of the border padding-box - the background is painted to
the outside edge of the padding content-box - the background is painted
within the content box
----------------------------------------------------------------------------------------------

Shorthand:- background: color image repeat attachment position

Add multiple background images. Example \#example1 { background-image:
url(img\_flwr.gif), url(paper.gif); background-position: right bottom,
left top; background-repeat: no-repeat, repeat; }
================================================================================================================

Border Properties:-
-
border-width: (thin, medium, thick, length) border-style: (none, solid,
dotted, dashed, double, groove, ridge, inset, outset) border-color:
(color)

border-image: source slice width outset repeat|initial|inherit;
border-image-source: (url()) border-image-slice:
(number,%,fill,initial,inherit) border-image-width: (length, number,
initial, inherit) border-image-repeat: (stretch(default), repeat, round,
initial, inherit)

border-left-width: border-left-color: border-left-style:
border-right-width: border-right-color: border-right-style:
border-top-width: border-top-color: border-top-style:
border-bottom-width: border-bottom-color: border-bottom-style:
border-radius: border-top-right-radius: border-bottom-right-radius:
border-bottom-left-radius: border-top-left-radius: border-collapse:
(collapse, separate)

box-shadow: (none, [x-axis-shadow-length, y-axisshadow-length,
spread-radius1, spread-radius2, color, inset])

Shorthand:- border: width style color

---
Outline Properties:-
--
An outline is a line drawn outside the element's border.

outline-color: (color) outline-style: (none, solid, dotted, dashed,
double, groove, ridge, inset, outset) outline-width: (thin, medium,
thick, length) outline-offset: (inherit, offset)
-----

Box Model Properties:-
--
width: (auto, length, %, initial, inherit) height: (auto, length, %)
max-height: (none, length, %) max-width: (none, length, %) min-height:
(none, length, %) min-width: (none, length, %)

Important: When you set the width and height properties of an element
with CSS, you just set the width and height of the content area. To
calculate the full size of an element, you must also add padding,
borders and margins.!

margin: top right bottom left

margin-top: (auto, length, %) margin-right: (auto, length, %)
margin-bottom: (auto, length, %) margin-left: (auto, length, %)
------
Box Sizing: box-sizing: (border-box, content-box(default))

The CSS box-sizing property allows us to include the padding and border
in an element's total width and height.

By default, the width and height of an element is calculated like this:
width + padding + border = actual width of an element height + padding +
border = actual height of an element

Since the result of using the box-sizing: border-box; is so much better,
many developers want all elements on their pages to work this way.

Applying this to all elements is safe and wise:

   { box-sizing: border-box; }

---
Margin Collapse Top and bottom margins of elements are sometimes
collapsed into a single margin that is equal to the largest of the two
margins.

This does not happen on left and right margins! Only top and bottom margins.

padding: top right bottom left

padding-top: (length, %) padding-right: (length, %) padding-bottom:
(length, %) padding-left: (length, %)

Padding and Element Width If an element has a specified width, the
padding added to that element will be added to the total width of the
element. This is often an undesirable result.

i.e: Here the actual width will be 325px

div { width: 300px; padding: 25px; }

To keep the width at 300px, no matter the amount of padding, you can use the box-sizing property.

float: (none, left, right)

clear: (left, right, both, none)

If an element is taller than the element containing it, and it is
floated, it will "overflow" outside of its container. Then we can add
overflow: auto; to the containing element to fix this problem

Display: The display property is the most important CSS property for
controlling layout. The display property specifies if/how an element is
displayed.

display: (none, inline, block, inline-block, flex, inline-flex, grid,
inline-grid, contents, list-item, run-in, table, inline-table,
table-row-group, table-header-group, table-footer-group, table-row,
table-column-group, table-column, table-cell, table-caption, ruby,
ruby-base, ruby-text, ruby-base-group, ruby-text-group)

visibility: (hidden) -> Hides an element, but its space is occupied

display: none; is commonly used with JavaScript to hide and show
elements without deleting and recreating them. It also hides the space
taken by that element & element does not occupy space.

display:block: 1.Element starts with new line 2.Takes full width
3.Height & width can be applied

display:inline: 1.not starts with new line 2.Does not take full width
3.no height and width(including no top bottom margin)

display:inline-block: 1.not starts with new line 2.Does not take full
width 3.Height & width can be applied

Overflow: The CSS overflow property controls what happens to content
that is too big to fit into an area. overflow: (visible, hidden, scroll,
auto, no-display, no-content, overflow-x, overflow-y) overflow-x:
(visible, hidden, auto) overflow-y: (visible, hidden, auto)

-------
CSS Positioning:-
---
There are five different position values:

postion: (static(default), relative, absolute, fixed, sticky)

top: (auto, %, length) bottom: (auto, %, length) left: (auto, %, length)
right: (auto, %, length)

-An element with position: static; is not positioned in any special way;
it is always positioned according to the normal flow of the page.

-An element with position: relative; is positioned relative to its
normal position. Setting the top, right, bottom, and left properties of
a relatively-positioned element will cause it to be adjusted

-An element with position: fixed; is always stays in the same place even
if the page is scrolled. The top, right, bottom, and left properties are
used to position the element.

-An element with position: absolute; is positioned relative to the
nearest positioned ancestor. However; if an absolute positioned element
has no positioned ancestors, it uses the document body, and moves along
with page scrolling.

-An element with position: sticky; is positioned based on the user's
scroll position. A sticky element toggles between relative and fixed,
depending on the scroll position. It is positioned relative until a
given offset position is met in the viewport - then it "sticks" in place
(like position:fixed). Note: A "positioned" element is one whose
position is anything except static.

The z-index property specifies the stack order of an element

z-index: (auto, number) -\> To use this, element should be positioned
(relative/fixed/absolute) -\>An element can have a positive or negative
stack order:
---
Text Properties:-
--

color: (color) direction: (ltr, rtl, inherit) text-align: (start, end,
left, right, center, justify) vertical-align: (top, middle, bottom)
text-align-last: (start, end, left, right, center, justify)
text-decoration(none, underline, overline, line-through, blink)
text-transform: (none, lowercase, uppercase, capitalize) text-indent:
(length, %) text-shadow: [horizontal-shadow vertical-shadow blur-value
color] text-overflow: (none, clip, ellipsis)

line-height: (length) letter-spacing: (normal, length, %) word-spacing:
(normal, length, %) word-wrap: (normal, nowrap, break-word) word-break:
(normal, keep-all, loose, break-strict, break-all) white-space: (normal,
pre, nowrap, pre-wrap, pre-line)
writing-mode: (vertical-lr, vertical-rl)
----
Font Properties:-
--

font-size: (xx-small, x-small, small, medium, large, x-large, xx-large,
smaller, larger, inherit, length, %) font-family: (serif, sans-serif,
monospace, cursive, fantasy, font-name) font-style: (normal, italic,
oblique) font-weight: (normal, bold, bolder, ligher, value(100-900))
font-varient: (normal, small-caps)

Shorthand: font: font-style font-variant font-weight
font-size/line-height font-family;

Note: If the font name is more than one word, it must be in quotation
marks, like: "Times New Roman".

The font-family property should hold several font names as a "fallback"
system, to ensure maximum compatibility between browsers/operating
systems.

Web safe fonts are fonts that are universally installed across all
browsers and devices. The following list are the best web safe fonts for
HTML and CSS:

Arial (sans-serif) Verdana (sans-serif) Helvetica (sans-serif) Tahoma
(sans-serif) Trebuchet MS (sans-serif) Times New Roman (serif) Georgia
(serif) Garamond (serif) Courier New (monospace) Brush Script MT
(cursive)

use fonts.google.com to use google fonts i.e add this in html file:-
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
and add font-family: 'Sofia', arial in css

Add the fire effect to the "Sofia" font:
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia&effect=fire">

<h1 class="font-effect-fire">
Sofia on Fire
</h1>
---

Link:-
---
The four links states are:

a:link - a normal, unvisited link a:visited - a link the user has
visited a:hover - a link when the user mouses over it a:active - a link
the moment it is clicked

When setting the style for several link states, there are some order
rules:

a:hover MUST come after a:link and a:visited a:active MUST come after
a:hover
----
UI:
--
cursor: (auto, crosshair, default, pointer, move, re-size, neresize,
nwresize, nresize, seresize, sw-resize, sresize, w-resize, text, wait,
help, all-scroll, cell, grab, not-allowed, progress, zoom-in, zoom-out,
url, ...)

color: (inherit, color)

opacity: (inherit, number)

filter: none | blur() | brightness() | contrast() | drop-shadow() |
grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia()
| url();

-webkit-box-reflect: [(below, above, left, right) offset]

icon: (auto, inherit, url())

resize: (none, horizontal, vertical, both)

Note: resize works on block elements only & overflow should not be
visible
---
clear: (none, left, right, both) The clear property specifies what
elements can float beside the cleared element and on which side.

object-fit: (fill, contain, cover, none, scale-down) -\> specify how an
<img> or
<video> 
should be resized to fit its container. -It preserves the aspect ratio
of image or video. -object-fit: contain; the image keeps its aspect
ratio, but is resized to fit within the given dimension. -If we use
object-fit: fill; the image is resized to fill the given dimension. If
necessary, the image will be stretched or squished to fit. -If we use
object-fit: none; the image is not resized.

object-position: ((top left | top center | top right | center left |
center center | center right | bottom left | bottom center | bottom
right

                    x-% y-%
                    x-px y-px))

---
Table:
--
border-collapse: (separate, collapse) border-spacing: [length length]
empty-cells: (show, hide) caption-side: (top, bottom, left, right)
table-layout: (auto, fixed)

To specify table borders in CSS, use the border property.

table, th, td { border: 1px solid black; }

Full table width:

table { width: 100%; }

To make striped table use nth-child(): tr:nth-child(even){
background-color: \#f2f2f2; }

To make table responsive: Add a container element (like
<div>
) with overflow-x:auto around the
<table> 
element to make it responsive:
<div style="overflow-x:auto;">

<table>
... table content ...
</table>

</div>

Colors in CSS:- 
--
Colors are specified using predefined color names, or
RGB, HEX, HSL, RGBA, HSLA values. CSS/HTML support 140 standard color
names. Some examples: Tomato Orange DodgerBlue MediumSeaGreen Gray
SlateBlue red LightGray

1.RGB Value rgb(red, green, blue) white = rgb(0,0,0) black =
rgb(255,255,255) red = rgb(255,0,0), green = rgb(0,255,0), blue =
rgb(0,0,255)

2.RGBA Value rgba(red, green, blue, alpha) he alpha parameter is a
number between 0.0 (fully transparent) and 1.0 (not transparent at all)

3.HEX Value \#rrggbb Where rr (red), gg (green) and bb (blue) are
hexadecimal values between 00 and ff (same as decimal 0-255). For
example, \#ff0000 is displayed as red, because red is set to its highest
value (ff) and the others are set to the lowest value (00). black =
\#000000, white = \#ffffff, red = \#ff0000, green = \#00ff00, blue =
\#0000ff

4.HSL Value hsl(hue, saturation, lightness)

Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is
green, and 240 is blue. Saturation is a percentage value, 0% means a
shade of gray, and 100% is the full color. Lightness is also a
percentage, 0% is black, 50% is neither light or dark, 100% is white

5.HSLA Value hsla(hue, saturation, lightness, alpha) The alpha parameter
is a number between 0.0 (fully transparent) and 1.0 (not transparent at
all)

CSS Color Keywords: -The transparent keyword is used to make a color
transparent.

-The currentcolor keyword is like a variable that holds the current
value of the color property of an element. Example In this example the
border color of the
<div> 
element will be blue, because the text color of the
<div> 
element is blue:

div { color: blue; border: 10px solid currentcolor; }

-The inherit keyword specifies that a property should inherit its value
from its parent element. The inherit keyword can be used for any CSS
property, and on any HTML element.
----

Gradients:- 
--
CSS gradients let you display smooth transitions between two
or more specified colors. CSS defines two types of gradients: 1)Linear
Gradients (goes down/up/left/right/diagonally) 2)Radial Gradients
(defined by their center)

Linear Gradients:

To create a linear gradient you must define at least two color stops.

Syntax:- background: linear-gradient(direction/angle, color1, color2,
....)

Directions: to bottom (this is default): background-image:
linear-gradient(red, yellow); -to left -to right -to top

Diagonally:

-to top left -to top right -to bottom left -to bottom right

Using Angles:- background-image: linear-gradient(180deg, red, yellow);

Repeating a linear-gradient:- The repeating-linear-gradient() function
is used to repeat linear gradients: repeating-linear-gradient(red,
yellow 10%, green 20%);

Radial Gradients: A radial gradient is defined by its center.

background-image: radial-gradient(shape size at position, start-color,
..., last-color)

Radial Gradient - Evenly Spaced Color Stops (this is default):-
background-image: radial-gradient(red, yellow, green);

Radial Gradient - Differently Spaced Color Stops:- background-image:
radial-gradient(red 5%, yellow 15%, green 60%);

Set Shape:- background-image: radial-gradient(circle, red, yellow,
green);

Repeating a radial-gradient:- repeating-radial-gradient(red, yellow 10%,
green 15%);
---
CSS 2D & 3D Transforms:-
---
CSS transforms allow you to move, rotate, scale, and skew elements. We
cannot apply transform on inline elements.

transform: Applies a 2D or 3D transformation to an element

With transform property you can use the following 2D transformation
methods: transform: (none,

translate(x-axis-length, y-axis-length), translate3d(x,y,z),
translateX(length), translateY(length), translateZ(length),
rotate(angle), rotateX(angle), rotateY(angle), rotateZ(angle),
rotate3d(x,y,z,angle) scale(width, height), scale3d(x,y,z)
scaleX(width), scaleY(height), skew(x-axis-angle, y-axis-angle)
skewX(angle), skewY(angle),
matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY()) )
matrix3d: (n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n)

perspective: (length) transform-style:
flat(default)|preserve-3d|initial|inherit; -\> This property must be
used together with the transform property.

perspective-origin: x-axis y-axis|initial|inherit;

-The perspective property defines how far the object is away from the
user. So, a lower value will result in a more intensive 3D effect than a
higher value.

-The perspective-origin property defines at from which position the user
is looking at the 3D-positioned element.

-The transform-origin property allows you to change the position of
transformed elements. Transform, transforms the element from its center,
but using transform-origin we can change x and y axis position.

-The transform-style property specifies how nested elements are rendered
in 3D space.

-The backface-visibility property defines whether or not the back face
of an element should be visible when facing the user.

-The matrix() method combines all the 2D transform methods into one. The
matrix3D() Defines a 3D transformation, using a 4x4 matrix of 16 values

transform-origin:

transform-origin: x-axis y-axis z-axis|initial|inherit;

x-axis -\> (left, right, center, length, %) y-axis -\> (top, bottom,
center, length, %) z-axis -\> (length)
----
CSS Transitions:-
----
CSS transitions allows you to change property values smoothly, over a
given duration.

transition-property: (none, property-name, all); transition-duration:
(time in s or ms) transition-delay: (time in s or ms)
transition-timing-function: (linear, ease(default), ease-in, ease-out,
cubic-bezier(n,n,n,n))

ease - specifies a transition effect with a slow start, then fast, then
end slowly (this is default) linear - specifies a transition effect with
the same speed from start to end ease-in - specifies a transition effect
with a slow start ease-out - specifies a transition effect with a slow
end ease-in-out - specifies a transition effect with a slow start and
end cubic-bezier(n,n,n,n) - lets you define your own values in a
cubic-bezier function

Shorthand: transition: property duration transition-timing-function
delay;
----
CSS Animations:- 
---
CSS allows animation of HTML elements without using
JavaScript or Flash!

When you specify CSS styles inside the @keyframes rule, the animation
will gradually change from the current style to the new style at certain
times.

animation-name: (none, keyframe-rule-name) animation-duration: (time in
s or ms) animation-delay: (time in s or ms) animation-iteration-count:
(inherit, number, infinite) animation-direction: (normal, reverse,
alternate, alternate-reverse) animation-timing-function: (linear,
ease(default), ease-in, ease-out, cubic-bezier(n,n,n,n))
animation-running-state: (running, paused) animation-fill-mode: (none,
forwards, backwards, both)

Shorthand: animation: name duration animation-delay-function delay
animation-iteration-count animation-direction;

normal - The animation is played as normal (forwards). This is default
reverse - The animation is played in reverse direction (backwards)
alternate - The animation is played forwards first, then backwards
alternate-reverse - The animation is played backwards first, then
forwards

@keyframes example { from {background-color: red;} to {background-color:
yellow;} }

@keyframes example2 { 10% {background-color: red;} 50%
{background-color: yellow;} 100% {color: black} }

div { width: 100px; height: 100px; background-color: red;
animation-name: example; animation-duration: 4s; }

The animation-fill-mode property specifies a style for the target
element when the animation is not playing (before it starts, after it
ends, or both).

The animation-fill-mode property can have the following values:

none - Default value. Animation will not apply any styles to the element
before or after it is executing forwards - The element will retain the
style values that is set by the last keyframe (depends on
animation-direction and animation-iteration-count) backwards - The
element will get the style values that is set by the first keyframe
(depends on animation-direction), and retain this during the
animation-delay period both - The animation will follow the rules for
both forwards and backwards, extending the animation properties in both
directions
---
CSS Flexbox:-
-----
-The Flexible Box Layout Module, makes it easier to design flexible
responsive layout structure without using float or positioning.

-It is better way to align items into container.

-Flexbox is flexible box which helps to create responsive layout

-We can change order of flex-items without modifying html code.

display: (flex, inline-flex);

Flex Container Properties:

flex-direction: (row(default), column, row-reverse, column-reverse)
flex-wrap: (nowrap(default), wrap, wrap-reverse) flex-flow:
[flex-direction flex-wrap] ---\> Shorthand for above 2 properties
justify-content: (flex-start, flex-end, center, space-around,
space-between, space-evenly) align-items: (flex-start, flex-end, center,
strech(default), baseline) align-content: (flex-start, flex-end, center,
space-around, space-between, space-evenly, strech(default))
----
Flex Items Properties:
---
order: (number) -\> default is 0, higher the order, later it will show
in container flex-grow: (number) -\> default is 0 flex-shrink (number)
-\> default is 0 flex-basis: (length,%) -\> specifies the initial length
of a flex item(if flex-direction is row it acts as width else height).
align-self: (flex-start, flex-end, center, strech(default)) flex:
[flex-grow flex-shrink flex-basis]

Example The flex container becomes flexible by setting the display
property to flex: A flex container with three flex items:

<div class="flex-container">

<div>

1

</div>

<div>

2

</div>

<div>

3

</div>

</div>

----
CSS Multiple Columns:-
---

The CSS multi-column layout allows easy definition of multiple columns
of text - just like in newspapers:

column-count: (auto, number) column-gap: (normal, length)

column-rule-style: (none, solid, dotted, dashed, double, groove, ridge,
inset, outset) column-rule-width: (thin, medium, thick, length)
column-rule-color: (color)

column-rule: [column-rule-width column-rule-style column-rule-color]

column-span: (1, all) column-width: (auto, length) -\> specifies minimal
optimal width for column

column: [column-width column-count] -\> Shorthand

----
CSS Grid Layout Module:-
--

-The CSS Grid Layout Module offers a grid-based layout system, with rows
and columns, making it easier to design web pages without having to use
floats and positioning.

-Grid works for 2 dimentional alignment, flexbox is good for space
distribution.

display: (grid, inline-grid)

grid-template-columns: [column1\_length column2\_length column3\_length
......] grid-template-rows: [row1\_length row2\_length row3\_length
......] grid-template: [grid-template-rows grid-template-columns]
grid-template-areas: 'grid-area-name1 grid-area-name1 ....'
'grid-area-name1 grid-area-name2 ....'
'....................................'

grid-column-gap: (none, length, %) grid-row-gap: (none, length, %)
grid-gap: [grid-column-gap grid-row-gap]

grid-column-start: (grid\_line\_number, span number) grid-column-end:
(grid\_line\_number, span number) grid-colum:
[grid-column-start/grid-column-end]

grid-row-start: (number, span number) grid-row-end: (number, span
number) grid-row: [grid-row-start/grid-row-end]

grid-area: (grid\_item\_name,
[grid-row-start/grid-column-start/grid-row-end/grid-column-end])

grid-template-areas: [grid\_item\_names....] -\> Specifies how to
display columns and rows, using named grid items

grid-auto-rows: (length, %) grid-auto-columns: (length, %)
grid-auto-flow: (row, column, dense, row dense, column dense)

align-content: (start, end, center, space-around, space-between,
space-evenly, strech(default))

Name all items, and make a ready-to-use webpage template:

.item1 { grid-area: header; } .item2 { grid-area: menu; } .item3 {
grid-area: main; } .item4 { grid-area: right; } .item5 { grid-area:
footer; }

.grid-container { grid-template-areas: 'header header header header
header header' 'menu main main main right right' 'menu footer footer
footer footer footer'; }

----
CSS Pseudo-classes:- 
---
A pseudo-class is used to define a special state of
an element. 
Syntax:-

selector:pseudo-class { property: value; }

:active: an activated element :focus: an element while the element has
focus :link: an unvisited link :visited: an visited link :hover: an
element when you mouse over it :active: an active link :disabled: an
element while the element is disabled :enabled: an element while the
element is enabled :checked: an element that is checked :selection: an
element that is currently selected or highlighted by the user :empty:
selects every elements that has no children. :lang: allows the author to
specify a language to use in a specified element
:nth-child(n/even/odd/pattern(2n+1)): an element that is the n-th
sibling :nth-last-child(n): an element that is the n-th sibling counting
from the last sibling :first-child: an element is the first sibling
:last-child: an element is the last sibling :only-child: an element that
is the only child :first-of-type: an element that is the first sibling
of its type :last-of-type: an element that is the last sibling of its
type :nth-of-type(n): an element that is nth sibling of its type
:nth-last-of-type(n): an element that is nth sibling of its type
counting from last :only-of-type: an element that is the only child of
its type :root: root element of the document :not(selector): Selects
every element that is not a specified selector :target: a target element
as specified by a target in a URL

:valid: input:valid: Selects all <input> elements with a valid value
:required input:required: Selects <input> elements with a "required"
attribute specified :optional input:optional: Selects <input> elements
with no "required" attribute :out-of-range input:out-of-range: Selects
<input> elements with a value outside a specified range :read-only
input:read-only: Selects <input> elements with a "readonly" attribute
specified :read-write input:read-write: Selects <input> elements with no
"readonly" attribute
---

CSS Pseudo-elements:- 
---
A CSS pseudo-element is used to style specified
parts of an element. For example, it can be used to: Style the first
letter, or line, of an element Insert content before, or after, the
content of an element

Syntax:- selector::pseudo-element { property: value; }

::first-letter: Adds special style to the first letter of a text
::first-line: Adds special style to the first line of a text
::selection: Adds special style to the element when it is selected by
the user ::before: Inserts some content before the content of an element
::after: Inserts some content after the content of an element

initial & inherit keyword: The initial keyword is used to set a CSS
property to its default value. The inherit keyword specifies that a
property should inherit its value from its parent element.
---
Units in CSS:-
---
1.Absolute Units:

cm - centimeters mm - millimeters in - inches (1in = 96px = 2.54cm) px
\* - pixels (1px = 1/96th of 1in) pt - points (1pt = 1/72 of 1in) pc -
picas (1pc = 12 pt)

2.Relative Units:

em - Relative to the font-size of the element (2em means 2 times the
size of the current font) rem - Relative to font-size of the root
element vw - Relative to 1% of the width of the viewport* vh - Relative
to 1% of the height of the viewport* vmin - Relative to 1% of
viewport's\* smaller dimension\
vmax - Relative to 1% of viewport's\* larger dimension % - Relative to
the parent element

\*Viewport = the browser window size. If the viewport is 50cm wide, 1vw
= 0.5cm.

----
CSS Variables - The var() Function:-
----
-The var() function is used to insert the value of a CSS variable.

-CSS variables have access to the DOM, which means that you can create
variables with local or global scope, change the variables with
JavaScript, and change the variables based on media queries.

-CSS variables can have a global or local scope.

-Global variables can be accessed/used through the entire document,
while local variables can be used only inside the selector where it is
declared.

-To create a variable with global scope, declare it inside the :root
selector. The :root selector matches the document's root element.

Example:

:root { --blue: \#1e90ff; --white: \#ffffff; }

body { background-color: var(--blue); }

Note: The variable name must begin with two dashes (--) and it is case sensitive!

---

CSS The !important Rule:
---
The !important rule in CSS is used to add more importance to a
property/value than normal. In fact, if you use the !important rule, it
will override ALL previous styling rules for that specific property on
that element!

Example: \#myid { background-color: blue; }

.myclass { background-color: gray; }

p { background-color: red !important; }

----
CSS Media Query:
----
Media query is a CSS technique introduced in CSS3. It uses the @media
rule to include a block of CSS properties only if a certain condition is
true.

Example If the browser window is 600px or smaller, the background color
will be lightblue:

@media only screen and (max-width: 600px) { body { background-color:
lightblue; } }

If the browser window is 600px or greater, the background color will be
lightblue:

@media only screen and (min-width: 600px) { body { background-color:
green; } }

Orientation: Portrait / Landscape Media queries can also be used to
change layout of a page depending on the orientation of the browser.

Example

@media only screen and (orientation: landscape) { body {
background-color: lightblue; } }

---
Print style in CSS:-
----

@media screen{ style for screen }
@media print{ style for print }
@media only screen{style only for screen}
@media only print{style only for print}
---
The CSS @font-face Rule:- 
---
Web fonts allow Web designers to use fonts that
are not installed on the user's computer. When you have found/bought the
font you wish to use, just include the font file on your web server, and
it will be automatically downloaded to the user when needed.

@font-face { font-family: myFirstFont; src: url(sansation\_light.woff);
}

div { font-family: myFirstFont; }

