# stylus-grid
A simple and semantic grid system written in Stylus.<br/>
Example page at [http://alexisgaillard.github.io/stylus-grid/](http://alexisgaillard.github.io/stylus-grid/)

### Get started
By default the mixin output a 12 columns fluid grid system with 1% of gutter and a maximum width of 1272px.
```stylus
@import "stylus-grid"
grid()
```

Your markup should look like this:
```html
<div class="Grid">;
  <div class="Col__1">...</div>
  <div class="Col__11">...</div>
  <div class="Col__2">...</div>
  <div class="Col__10">...</div>
  ...
</div>
```

We can add margin before or after an element with the ".Pre / .Post" classes:
```html
<div class="Grid">;
  <div class="Col__2 Pre__2 Post__8">...</div>
  <div class="Col__2 Pre__4 Post__6">...</div>
  ...
</div>
```

For a 12 columns fluid grid system with 1% of gutter placed inside the columns:
```stylus
grid(Grid, Col, 12, 1%, inner)
```

For a 5 columns fluid grid system with 2% of gutter:
```stylus
grid(Grid, Col, 5, 2%)
```

All options available:
```stylus
  container-selector-name = Grid, //parent container class
  column-number-selector-name = Col, //will be suffixed with __{column}
  column-number = 12, // minimum >0
  gutter-w = 1%, //percentage can be set to 0
  gutter-inner = false, //if true set de gutters as padding instead of margin
  max-width = 1272px, //value in px or false
  pre-post = true, //if false avoid the output of the .Pre and .Post classes
  nesting = false, //output CSS reuired for columns nesting
  deepness = 6 //define the number of decimals on the percentage's width values
```
## Credits

Developed by [Alexis Gaillard](https://alexisgaillard.com/). Licensed under [MIT](http://opensource.org/licenses/mit-license.php).
