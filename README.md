# stylus-grid
A simple and semantic grid system written in Stylus

### Get started
By default the mixin output a 12 column fluid grid system with 1% of gutter and a maximum width of 1272px.
```stylus
@import "stylus-grid"
grid()
```

Your markup should look like this:
```stylus
<div class="Grid">;
  <div class="Col__1">...</div>
  <div class="Col__11">...</div>
  <div class="Col__2">...</div>
  <div class="Col__10">...</div>
  ...
</div>
```

## Credits

Developed by [Alexis Gaillard](https://alexisgaillard.com/). Licensed under [MIT](http://opensource.org/licenses/mit-license.php).
