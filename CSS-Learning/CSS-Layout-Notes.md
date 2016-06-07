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
- Possible values:
  - `static`: default value, not positioned in any special way
  - `relative`: behaves the same as static unless you change the `top` `right`
  `bottom` `left` properties, which will offset it a lil bit
  - `fixed`: positioned relative to the viewport (it can stay somewhere even
  if u scroll). Uses same properties as relative
  - `absolute`: like `fixed`, but relative to the nearest positioned ancestor
  (whatever that means lmao). Positioned means not `static`.
    - can be used in conjunction with `relative` usually
