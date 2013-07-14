# Bits.scss flexible embed

Component for responsive, intrinsic ratio embeds.

Read more about [Bits.scss toolkit](https://github.com/bits-scss/bits.scss).

## Installation

* __Bower:__ `bower install --save bits-scss-flex-embed`
* __Download:__ [zip](https://github.com/bits-scss/flex-embed/zipball/master), [tar.gz](https://github.com/bits-scss/flex-embed/tarball/master)
* __Git:__ `git clone https://github.com/bits-scss/flex-embed.git`

## Available SASS variables

* `bits-components-ns` - components namespace, defaults to 'bits-'
* `bits-flex-embed-ratios-x` - list of `x` values in an `x:y` ratio (eg. 4, 16)
* `bits-flex-embed-ratios-y` - list of `y` values in an `x:y` ratio (eg. 3, 9)

## Available classes

* `FlexEmbed` - core responsive embed component with no dimensions
* `FlexEmbed--XbyY` - modifier classes for X:Y aspect ratio embed (generated using SASS)
* `FlexEmbed-item` - sub-object class for the media that is being embedded
  (optional for `iframe`, `embed`, and `object` elements)

## Usage

Like many Bits.scss components, `bits-scss-flex-embed` relies on a base component class that is
extended by any number of additional modifier classes.

```html
<div class="FlexEmbed FlexEmbed--16by9">
  [iframe|object|embed]
</div>

<div class="FlexEmbed FlexEmbed--4by3">
  <img class="FlexEmbed-item" src="…" alt="">
</div>
```

The `bits-scss-flex-embed` component can be extended with additional aspect ratios if your
application makes use of multi-media embeds that require them. For example, to
create a 2.35:1 aspect ratio, modify these variables:

```scss
$bits-flex-embed-ratios-x: (4 16 47) !default; /* 2 */
$bits-flex-embed-ratios-y: (3 9  20) !default; /* 3 */
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