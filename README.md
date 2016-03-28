# stylus-grid
A simple and semantic grid system written in Stylus.
[Demo page](http://stylus-grid.movingislands.com).

### Dependencies
  * [stylus](https://github.com/LearnBoost/stylus)

### Get started
Install the stylus-grid.styl in your mixin folder, import, and init as follow:
```stylus
@import "stylus-grid"
grid()
```
By default the mixin output the CSS for a 12 columns fluid grid system with 1% of gutter and a maximum width of 1272px:
```css
clearfix:after {
  content: "";
  display: table;
  clear: both;
}
.Grid {
  position: relative;
  max-width: 1272px;
  width: 99%;
  margin: 0.5% auto;
  margin-top: 0;
  margin-bottom: 0;
}
.Grid:after {
  content: "";
  display: table;
  clear: both;
}
[class*="Col__"] {
  padding-right: 0;
  padding-left: 0;
  float: Left;
}
.Col__1 {
  width: 7.333334%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__2 {
  width: 15.666667%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__3 {
  width: 24%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__4 {
  width: 32.333334%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__5 {
  width: 40.666667%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__6 {
  width: 49%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__7 {
  width: 57.333334%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__8 {
  width: 65.666667%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__9 {
  width: 74%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__10 {
  width: 82.333334%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__11 {
  width: 90.666667%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Col__12 {
  width: 99%;
  margin-right: 0.5%;
  margin-left: 0.5%;
}
.Pre__1 {
  margin-left: 8.833334%;
}
.Pre__2 {
  margin-left: 17.166667%;
}
.Pre__3 {
  margin-left: 25.5%;
}
.Pre__4 {
  margin-left: 33.833334%;
}
.Pre__5 {
  margin-left: 42.166667%;
}
.Pre__6 {
  margin-left: 50.5%;
}
.Pre__7 {
  margin-left: 58.833334%;
}
.Pre__8 {
  margin-left: 67.166667%;
}
.Pre__9 {
  margin-left: 75.5%;
}
.Pre__10 {
  margin-left: 83.833334%;
}
.Pre__11 {
  margin-left: 92.166667%;
}
.Post__1 {
  margin-right: 7.833334%;
}
.Post__2 {
  margin-right: 16.166667%;
}
.Post__3 {
  margin-right: 24.5%;
}
.Post__4 {
  margin-right: 32.833334%;
}
.Post__5 {
  margin-right: 41.166667%;
}
.Post__6 {
  margin-right: 49.5%;
}
.Post__7 {
  margin-right: 57.833334%;
}
.Post__8 {
  margin-right: 66.166667%;
}
.Post__9 {
  margin-right: 74.5%;
}
.Post__10 {
  margin-right: 82.833334%;
}
.Post__11 {
  margin-right: 91.166667%;
}
```

Your markup should look like this:
```html
<div class="Grid">
  <div class="Col__1">...</div>
  <div class="Col__11">...</div>
  <div class="Col__2">...</div>
  <div class="Col__10">...</div>
  ...
</div>
```

We can add margin before or after an element with the ".Pre / .Post" classes:
```html
<div class="Grid">
  <div class="Col__2 Pre__2 Post__8">...</div>
  <div class="Col__2 Pre__4 Post__6">...</div>
  ...
</div>
```

For a 12 columns fluid grid system with 1% of gutter inside the columns:
```stylus
grid(Grid, Col, 12, 1%, inner)
```
Will output:
```css
clearfix:after {
  content: "";
  display: table;
  clear: both;
}
.Grid {
  position: relative;
  max-width: 1272px;
  width: 100%;
  margin-right: 0;
  margin-left: 0;
}
.Grid:after {
  content: "";
  display: table;
  clear: both;
}
[class*="Col__"] {
  margin-right: 0;
  margin-left: 0;
  float: Left;
}
.Col__1 {
  width: 7.333334%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__2 {
  width: 15.666667%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__3 {
  width: 24%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__4 {
  width: 32.333334%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__5 {
  width: 40.666667%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__6 {
  width: 49%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__7 {
  width: 57.333334%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__8 {
  width: 65.666667%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__9 {
  width: 74%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__10 {
  width: 82.333334%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__11 {
  width: 90.666667%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Col__12 {
  width: 99%;
  padding-right: 0.5%;
  padding-left: 0.5%;
}
.Pre__1 {
  margin-left: 8.383334%;
}
.Pre__2 {
  margin-left: 16.716667%;
}
.Pre__3 {
  margin-left: 25.05%;
}
.Pre__4 {
  margin-left: 33.383334%;
}
.Pre__5 {
  margin-left: 41.716667%;
}
.Pre__6 {
  margin-left: 50.05%;
}
.Pre__7 {
  margin-left: 58.383334%;
}
.Pre__8 {
  margin-left: 66.716667%;
}
.Pre__9 {
  margin-left: 75.05%;
}
.Pre__10 {
  margin-left: 83.383334%;
}
.Pre__11 {
  margin-left: 91.716667%;
}
.Post__1 {
  margin-right: 8.283334%;
}
.Post__2 {
  margin-right: 16.616667%;
}
.Post__3 {
  margin-right: 24.95%;
}
.Post__4 {
  margin-right: 33.283334%;
}
.Post__5 {
  margin-right: 41.616667%;
}
.Post__6 {
  margin-right: 49.95%;
}
.Post__7 {
  margin-right: 58.283334%;
}
.Post__8 {
  margin-right: 66.616667%;
}
.Post__9 {
  margin-right: 74.95%;
}
.Post__10 {
  margin-right: 83.283334%;
}
.Post__11 {
  margin-right: 91.616667%;
}
```

For a 5 columns fluid grid system with 2% of gutter:
```stylus
grid(Grid, Col, 5, 2%)
```

Will output:
```css
clearfix:after {
  content: "";
  display: table;
  clear: both;
}
.Grid {
  position: relative;
  max-width: 1272px;
  width: 98%;
  margin: 1% auto;
  margin-top: 0;
  margin-bottom: 0;
}
.Grid:after {
  content: "";
  display: table;
  clear: both;
}
[class*="Col__"] {
  padding-right: 0;
  padding-left: 0;
  float: Left;
}
.Col__1 {
  width: 18%;
  margin-right: 1%;
  margin-left: 1%;
}
.Col__2 {
  width: 38%;
  margin-right: 1%;
  margin-left: 1%;
}
.Col__3 {
  width: 58%;
  margin-right: 1%;
  margin-left: 1%;
}
.Col__4 {
  width: 78%;
  margin-right: 1%;
  margin-left: 1%;
}
.Col__5 {
  width: 98%;
  margin-right: 1%;
  margin-left: 1%;
}
.Pre__1 {
  margin-left: 21%;
}
.Pre__2 {
  margin-left: 41%;
}
.Pre__3 {
  margin-left: 61%;
}
.Pre__4 {
  margin-left: 81%;
}
.Post__1 {
  margin-right: 19%;
}
.Post__2 {
  margin-right: 39%;
}
.Post__3 {
  margin-right: 59%;
}
.Post__4 {
  margin-right: 79%;
}
```

All options available are:
```stylus
  container-selector-name = Grid, //parent container class
  column-number-selector-name = Col, //will be suffixed with __{column}
  column-number = 12, // minimum >0
  gutter-w = 1%, //percentage can be set to 0
  gutter-inner = false, //if true set de gutters as padding instead of margin
  max-width = 1272px, //value in px or false
  pre-post = true, //if false avoid the output of the .Pre and .Post classes
  nesting = false, //output CSS required for columns nesting
  deepness = 6 //define the number of decimals on the percentage's width values
```

A shortand to control responsive features will follow soon.

## Credits

Developed by [Alexis Gaillard](https://alexisgaillard.com/). Licensed under [MIT](http://opensource.org/licenses/mit-license.php).
