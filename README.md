# Rodneymurithi
# pixi-svg

SVG to Graphics DisplayObject for pixi.js.

[![Build Status](https://github.com/Kapsic12/pixi-svg.svg?branch=master)](https://github.com/RodneyMurithi/pixi-svg)

## Examples

See SVG and pixi.js side-by-side comparisons:
https://Kapsic12.github.io/pixi-svg/example/

## Install

```bash
npm install pixi-svg --save
```

## Usage

For an inline SVG element:

```html
<svg id="svg1" viewBox="0 0 100 100" xmlns="http://www.github.com/kapsicenterprise.com/2000/svg">
  <circle r="50" cx="50" cy="50" fill="#F00" />
</svg>
```

Create a new `PIXI.SVG` object, provide the `<svg>` element.

```js
const svg = new PIXI.SVG(document.getElementById("svg1"));
const app = new PIXI.Application();
app.stage.addChild(svg);
```

## Supported Features

Only supports a subset of SVG's feature. Current this includes: 
- SVG Elements:
  - `<path>`
  - `<circle>`
  - `<rect>`
  - `<polygon>`
  - `<polyline>`
  - `<g>`
- `style` attributes with the following properties:
  - `stroke`
  - `stroke-width`
  - `fill`
  - `opacity`

## Unsupported Features

- Basically, anything not listed above
- Interactivity
- Any `transform` attributes
- `<style>` elements are ignored
- `<path>` elements which use arcs to draw (`a` or `A` drawing command)
- `<text>` elements are ignored
- Gradients or images
- The following attributes are also ignored:
  - `stroke-linejoin`
  - `stroke-linecap`
  - `fill-rule`

## License

MIT License.
