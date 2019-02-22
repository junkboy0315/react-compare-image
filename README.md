# React Compare Image

Simple React component to compare two images using slider.

![img](https://react-compare-image.yuuniworks.com/anime.gif)

NOTE: [Vue.js Version](https://github.com/junkboy0315/vue-compare-image) is also available!

## Demo

[DEMO](https://react-compare-image.yuuniworks.com/)

## Features

- Simple
- Responsive (fit to the parent width)
- Size difference between two images handled correctly. Element size determined by following two factors:
  - width of the parent
  - right image's aspect ratio

## How to use

```cmd
yarn add react-compare-image

// or

npm install --save react-compare-image
```

```jsx
import ReactCompareImage from 'react-compare-image';

<ReactCompareImage
  leftImage="image1.jpg"
  rightImage="image2.jpg"
/>;
```

## Props

| Prop (\* required)       | type           | default | description                                                                                                 |
| ------------------------ | -------------- | :-----: | ----------------------------------------------------------------------------------------------------------- |
| leftImage \*             | string         |  null   | left image's url                                                                                            |
| rightImage \*            | string         |  null   | right image's url                                                                                           |
| sliderPositionPercentage | number (float) |   0.5   | Default line position (from 0 to 1)                                                                         |
| sliderLineWidth          | number (px)    |    2    | line width of slider (by pixel)                                                                             |
| sliderLineColor          | string         |    "#ffffff"    | line color of slider                                                                                     
| handleSize               | number (px)    |   40    | diameter of slider handle (by pixel)                                                                        |
| hover                    | boolean        |  false  | Whether to slide at hover                                                                                   |
| skeleton                 | element        |  null   | Element displayed while image is loading                                                                    |
| autoReloadSpan           | number (ms)    |  null   | If specified, the image is loaded again at the interval specified when loading images failed                |
| autoReloadLimit          | number (count) |   10    | Limitation on automatic reload retry count                                                                  |
| onSliderPositionChange   | function       |  null   | Callback function called each time the slider changes. The position (0 to 1) of the slider is passed as arg |
| leftImageCss             | object        |  {}  | Additional css for left image                                                                                  |
| rightImageCss            | object        |  {}  | Additional css for right image                                                                                 |

## Dependencies

- [css-element-queries](https://github.com/marcj/css-element-queries) to detect element resize event.
