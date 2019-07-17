# rc-virtual-list

React Virtual List Component which worked with animation.

[![NPM version][npm-image]][npm-url] [![build status][circleci-image]][circleci-url] [![Test coverage][coveralls-image]][coveralls-url] [![node version][node-image]][node-url] [![npm download][download-image]][download-url]

[npm-image]: http://img.shields.io/npm/v/rc-virtual-list.svg?style=flat-square
[npm-url]: http://npmjs.org/package/rc-virtual-list
[circleci-image]: https://img.shields.io/circleci/build/github/react-component/virtual-list/master.svg?style=flat-square
[circleci-url]: https://circleci.com/gh/react-component/virtual-list/tree/master
[coveralls-image]: https://img.shields.io/codecov/c/github/react-component/virtual-list/master.svg?style=flat-square
[coveralls-url]: https://codecov.io/gh/react-component/virtual-list
[node-image]: https://img.shields.io/badge/node.js-%3E=_6.0-green.svg?style=flat-square
[node-url]: http://nodejs.org/download/
[download-image]: https://img.shields.io/npm/dm/rc-virtual-list.svg?style=flat-square
[download-url]: https://npmjs.org/package/rc-virtual-list

## Development

```bash
npm install
npm start
open http://localhost:9001/
```

## Feature

- Support react.js
- Support animation
- Support IE11+

## Install

[![rc-virtual-list](https://nodei.co/npm/rc-virtual-list.png)](https://npmjs.org/package/rc-virtual-list)

## Usage

```js
import List from 'rc-virtual-list';

<List data={[0, 1, 2]} height={200} itemHeight={30} itemKey="id">
  {index => <div>{index}</div>}
</List>;
```

# API

## List

| Prop       | Description                                             | Type                                 | Default |
| ---------- | ------------------------------------------------------- | ------------------------------------ | ------- |
| children   | Render props of item                                    | (item, index, props) => ReactElement | -       |
| component  | Customize List dom element                              | string \| Component                  | div     |
| data       | Data list                                               | Array                                | -       |
| disabled   | Disable scroll check. Usually used on animation control | boolean                              | false   |
| height     | List height                                             | number                               | -       |
| itemHeight | Item minium height                                      | number                               | -       |
| itemKey    | Match key with item                                     | string                               | -       |

`children` provides additional `props` argument to support IE 11 scroll shaking.
It will set `style` to `visibility: hidden` when measuring. You can ignore this if no requirement on IE.
