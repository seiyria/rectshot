# rectshot
A small nodejs utility to get the color of a pixel on the desktop screen.

## Usage

`npm i rectshot`

```js
import rectshot from rectshot;

// synchronous usage - this gets the screen image to buffer at coordinate 100, 200 for a width of 200x200
const color = rectshot([100, 200, 200, 200], true);

// async usage - this gets the screen image to buffer at coordinate 100, 200 for a width of 200x200
pixcolor([100, 200, 200, 200], (err, buffer) => {

});
```

The return value will be a `Buffer`, containing the image data for the region.

## Restrictions

This uses [edge-js](https://github.com/agracio/edge-js), so it only runs on windows, and from a node environment - it will not work in the browser.