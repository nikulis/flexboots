#flexboots :boot::boot:

Flexboots is a lightweight css library for easily making layouts. It can achieve similar effects for which one might normally use [Bootstrap](http://getbootstrap.com), but has some more flexibility, among other advantages. Also works well in combination with Bootstrap.

##What can it do?

Check out the [demo](http://nikulis.github.io/flexboots/demo).

flexboots provides a simple wrapper to easily set up and work with css flexboxes.
> The CSS3 Flexible Box, or flexbox, is a layout mode providing for the arrangement of elements on a page such that the elements behave predictably when the page layout must accommodate different screen sizes and different display devices. For many applications, the flexible box model provides an improvement over the block model in that it does not use floats, nor do the flex container's margins collapse with the margins of its contents. 

> Many designers will find the flexbox model easier to use. Child elements in a flexbox can be laid out in any direction and can have flexible dimensions to adapt to the display space. Positioning child elements is thus much easier, and complex layouts can be achieved more simply and with cleaner code, as the display order of the elements is independent of their order in the source code.

Read the full CSS3 flexbox documentation on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes).

## Why is it better than Bootstrap?

**It's not *better* than Bootstrap**; flexboots (and css flexbox in general) just offers a different approach to layouts that may be advantageous, depending on the type of design you are trying to achieve.

Consider the following use case: you have an image with a corresponding block of text. You want to lay them out side-by-side on desktop reflowing to each be full-width on mobile. You do the following using Bootstrap's `col-`'s:

```html
<div class="row">
  <div class="col-md-4">
    <img src="picture.jpg" class="img-responsive"/>
  </div>
  <div class="col-md-8">
  	<p>[Lorem ipsum…]</p>
  </div>
</div>
```

This works pretty well, BUT, you notice that the picture is longer than the text (or the text is longer than the picture)… anyways, the column lengths are not equal. You want the columns' contents to be vertically centered to each other, something like `vertical-align: middle;`, but there isn't an easy (or syntactically clean) way to consistently do so.

Enter flexboots. The solution to this particular use case would be

```html
<div class="flexbox">
  <div class="flexitem one-third">
    <img src="picture.jpg" class="img-responsive"/>
  </div>
  <div class="flexitem two-thirds">
    <p>[Lorem ipsum…]</p>
  </div>
</div>
```

##Usage

Simply download flexboots.css and include it in your web project, like
```html
<link href="<path>/flexboots.css" rel="stylesheet" type="text/css" />
```

Making your first flexbox is as easy as
```html
<div class="flexbox">
  <div class="flexitem">
    some stuff
  </div>
  <div class="flexitem">
    some more stuff
  </div>
</div>
```

##Browser Support

Some browsers implement old, unofficial, and/or vendor-prefixed versions of the flexbox model in CSS3. flexboots should work as advertised on the following:

Desktop:
- Chrome 21+
- Firefox 28+
- IE 10+
- Opera 12.10+
- Safari 6.1+

Mobile:
- Firefox Mobile 28+
- Opera Mobile 15+
- Safari 7+

As you extend and further customize your designs and layouts using more advanced flexbox syntax, keep in mind that some browsers may not play kindly. For more info on browser compatibility, see [MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes#Browser_compatibility) and [CSS-Tricks](http://css-tricks.com/snippets/css/a-guide-to-flexbox/).