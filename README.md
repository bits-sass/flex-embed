# Bits.sass flexible embed

Component for responsive, intrinsic ratio embeds.

Read more about [Bits.sass toolkit](https://github.com/bits-sass/bits.sass).

## Installation

* __Bower:__ `bower install --save bits-sass-flex-embed`
* __Download:__ [zip](https://github.com/bits-sass/flex-embed/zipball/master), [tar.gz](https://github.com/bits-sass/flex-embed/tarball/master)
* __Git:__ `git clone https://github.com/bits-sass/flex-embed.git`

## Available SASS variables

* `bits-components-ns` - components namespace, defaults to 'bits-'
* `bits-flex-embed-ratios` - list of x:y ratios

## Available classes

* `FlexEmbed` - core responsive embed component with no dimensions
* `FlexEmbed--XbyY` - modifier classes for X:Y aspect ratio embed (generated using SASS)
* `FlexEmbed-item` - sub-object class for the media that is being embedded
  (optional for `iframe`, `embed`, and `object` elements)

## Usage

Like many Bits.sass components, `bits-sass-flex-embed` relies on a base component class that is
extended by any number of additional modifier classes.

```html
<div class="FlexEmbed FlexEmbed--16by9">
  [iframe|object|embed]
</div>

<div class="FlexEmbed FlexEmbed--4by3">
  <img class="FlexEmbed-item" src="…" alt="">
</div>
```

The `bits-sass-flex-embed` component can be extended with additional aspect ratios if your
application makes use of multi-media embeds that require them. For example, to
create a 2.35:1 aspect ratio, modify `bits-flex-embed-ratios` variable:

```scss
$bits-flex-embed-ratios: (
  (16, 9)
  (4, 3)
  (47, 20)
);
```

Alternatively, aspect ratios can be calculated programmatically and the
corresponding `padding-bottom` value applied using an inline style.

## Requirements

* Sass 3.2+

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 8+