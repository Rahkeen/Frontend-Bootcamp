## Learning CSS Layouts
[Following this guide](learnlayout.com)

#### `display` property

- Most imporant property for controlling Layout
- default is usually `block` or `inline`
  - `div` is a block element by default
  - `span` is an inline element by default
- `none` is also used to hide and show elements with JS
  - different from setting visibility, which would hide element but still take
  up space
- Plenty of other `display` properties, such as `flex` and `inline-block`

#### `margin: auto`

- setting the width of a block level element will prevent it from stretching out
to the edges of its container, you can then set the left/right margin to center
it horizontally
- fix this by utilizing the `max-width`, which will allow the browser to resize
the element

#### The BOX model

- when u set the width, the element can still appear to be bigger due to padding
/ border specs. You can solve this by mathing it out a bit, or you can use a
property called `box-sizing`, which is still kinda new and needs vendor prefixes

#### `position` property

- another important CSS property when it comes to making more sophisticated
Layouts
- Possible values
  - `static`: default value, not positioned in any special way
  - `relative`: behaves the same as static unless you change the `top` `right`
  `bottom` `left` properties, which will offset it a lil bit
  - `fixed`: positioned relative to the viewport (it can stay somewhere even
  if u scroll). Uses same properties as relative
  - `absolute`: like `fixed`, but relative to the nearest positioned ancestor
  (whatever that means lmao). Positioned means not `static`.
    - can be used in conjunction with `relative` usually

  Layout Example: http://codepen.io/rahkeen/pen/MeaJOG

#### `float`

- used for wrapping text around stuff like images
- use `clear` to make sure an element is placed after a floated element
- sometimes floated element will be larger than container, which setting the
container to `overflow: auto` will usually fix (called clearfix)

Layout Example: http://codepen.io/rahkeen/pen/NrGzVx

#### percent `width`

- measurement unit relative to the containing block
- can use it for layouts, but it can get a bit wonky at small sizes
- we need a better way to handle different screen sizes

#### media queries

- making sites respond to the browser and the device it is displayed on
- example `media` query: `media screen and (min-width:600px)`
- check out MDN documentation for more ways to use it
- also check out meta viewport

Layout Example: http://codepen.io/rahkeen/pen/QEjrVY

#### `display: inline-block`

- `inline-block` elements are like inline elements, except they can have a
width and a height
- example: create a grid of boxes that fills the browser width and wraps nicely
  - attempt 1: [using float](http://codepen.io/rahkeen/pen/LZpmwL)
  - attempt 2: [using inline-block](http://codepen.io/rahkeen/pen/WxQyNB)

Layout Example: http://codepen.io/rahkeen/pen/OXyEYJ

#### `column`

- a newer css property that allows for multi-column text
-  use `column-count` and `column-gap` for a block element

#### `flexbox`

- An awesome way to do layout, however it isn't very standardized. You can still
do a lot of cool things
- Center vertically in a div (WOW):
  - `.vertical-container {
    height: 300px;
    display: -webkit-flex;
    display:         flex;
    -webkit-align-items: center;
            align-items: center;
    -webkit-justify-content: center;
            justify-content: center;
  }`

Layout Example: http://codepen.io/rahkeen/pen/MeaXqJ

#### CSS Frameworks

[List of CSS Frameworks to help me not  want to kill myself](http://learnlayout.com/frameworks.html)
