# React Portal Tooltip [![Build Status](https://api.travis-ci.org/romainberger/react-portal-tooltip.svg?branch=master)](https://travis-ci.org/romainberger/react-portal-tooltip)

Awesome tooltips.

**Warning** The latest version on npm is compatible with React 0.14. For React 0.13 install the [0.6.4](https://github.com/romainberger/react-portal-tooltip/tree/v0.6.4) version.

![react tooltip](https://raw.githubusercontent.com/romainberger/react-portal-tooltip/master/react-portal-tooltip.gif)

## Installation

    $ npm install @weflex/react-portal-tooltip --save

## Documentation and demo

[http://romainberger.github.io/react-portal-tooltip/](http://romainberger.github.io/react-portal-tooltip/)

## Usage

```javascript
import React from 'react'
import ToolTip from 'react-portal-tooltip'

class MyComponent extends React.Component {
    state = {
        isTooltipActive: false
    }
    showTooltip() {
        this.setState({isTooltipActive: true})
    }
    hideTooltip() {
        this.setState({isTooltipActive: false})
    }
    render() {
        return (
            <div>
                <p id="text" onMouseEnter={::this.showTooltip} onMouseLeave={::this.hideTooltip}>This is a cool component</p>
                <ToolTip active={this.state.isTooltipActive} position="top" arrow="center" parent="#text">
                    <div>
                        <p>This is the content of the tooltip</p>
                        <img src="image.png"/>
                    </div>
                </ToolTip>
            </div>
        )
    }
}
```

### Props

* `active`: boolean, the tooltip will be visible if true
* `position`: top, right, bottom or left. Default to right
* `arrow`: center, right, left, top or bottom (depending on the position prop). No arrow when the prop is not sepecified
* `parent`: the tooltip will be placed next to this element
* `group`: string, necessary if you want several independant tooltips
* `style`: object, allows customizing the tooltip. Checkout the [example](https://github.com/romainberger/react-portal-tooltip/blob/master/example/src/style.js) for details.
* `transition`: number, set transition duration

## Development

```shell
# clone
$ git clone git@github.com:romainberger/react-portal-tooltip.git

# install the dependencies
$ npm install

# go to the example folder, then install more dependencies
$ cd example && npm install

# start the development server with hot reloading
$ npm start

# to build run this command from the root directory
$ npm build
```

## License

MIT
