# draft-js-multidecorators

[![Build Status](https://github.com/qnighy/draft-js-multidecorators/actions/workflows/ci.yml/badge.svg)](https://github.com/qnighy/draft-js-multidecorators/actions/workflows/ci.yml)
[![npm version](https://badge.fury.io/js/%40qnighy%2Fdraft-js-multidecorators.svg)](https://badge.fury.io/js/%40qnighy%2Fdraft-js-multidecorators)


> Combine multiple Draft's decorators into one.

### Installation

```
$ npm install @qnighy/draft-js-multidecorators
```

### Usage

```js
var Draft = require('draft-js');
var MultiDecorator = require('@qnighy/draft-js-multidecorators');

var decorator = new MultiDecorator([
    new SomeCustomDecorator(),

    // This decorator will have more priority:
    new Draft.CompositeDecorator([ ... ])
]);

var editorState = Draft.EditorState.createEmpty(decorator)
```

### See also

You can use [SimpleDecorator](https://github.com/Soreine/draft-js-simpledecorator) to easily build decorators.

