# draft-js-multidecorators

[![Build Status](https://github.com/qnighy/draft-js-multidecorators/actions/workflows/ci.yml/badge.svg)](https://github.com/qnighy/draft-js-multidecorators/actions/workflows/ci.yml)
[![NPM version](https://badge.fury.io/js/draft-js-multidecorators.svg)](http://badge.fury.io/js/draft-js-multidecorators)


> Combine multiple Draft's decorators into one.

### Installation

```
$ npm install draft-js-multidecorators
```

### Usage

```js
var Draft = require('draft-js');
var MultiDecorator = require('draft-js-multidecorators');

var decorator = new MultiDecorator([
    new SomeCustomDecorator(),

    // This decorator will have more priority:
    new Draft.CompositeDecorator([ ... ])
]);

var editorState = Draft.EditorState.createEmpty(decorator)
```

### See also

You can use [SimpleDecorator](https://github.com/Soreine/draft-js-simpledecorator) to easily build decorators.

