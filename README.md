# doc.js

_dco.js_ is a set of basic helpers for formatting and writing in-code docs.

## Contents
- [doc.js](#docjs)
  - [Contents](#contents)
  - [Installation](#installation)
    - [`normalizeIndent(..)` / `normalizeTextIndent(..)` / `doc` / `text`](#normalizeindent--normalizetextindent--doc--text)
  - [License](#license)


## Installation

```shell
$ npm install ig-doc
```

Include the code, this is compatible with both [node's](https://nodejs.org/) and
[RequireJS'](https://requirejs.org/) `require(..)`
```javascript
var object = require('ig-doc')
```


### `normalizeIndent(..)` / `normalizeTextIndent(..)` / `doc` / `text`

Align _code_ to shortest leading white-space
```
normalizeIndent(<text>)
normalizeIndent(<text>, <tab-size>)
normalizeIndent(<text>, <tab-size>, <leading-tabs>)
	-> <text>
```

This is used to format `.toString(..)` return values for nested functions
to make source printing in console more pleasant to read.

`tab_size` defaults to `object.TAB_SIZE`

`leading_tabs` defaults to `object.LEADING_TABS`


A shorthand to `normalizeIndent(..)` optimized for text rather than code
```
normalizeTextIndent(..)
	-> <text>
```

This ignores `object.LEADING_TABS` and `leading_tabs` is 0 by default.


`doc` and `text` are template string versions of `normalizeIndent(..)` and `normalizeTextIndent(..)` respectively.


<!-- XXX Examples -->


## License

[BSD 3-Clause License](./LICENSE)

Copyright (c) 2016-2021, Alex A. Naanou,  
All rights reserved.


<!-- vim:set ts=4 sw=4 spell : -->
