[![venti](venti.png)](https://github.com/will123195/venti)

**Global State for React**

[![Build Status](https://travis-ci.org/will123195/venti.svg?branch=master)](https://travis-ci.org/will123195/venti)

## Overview

A very simple alternative to Redux

## Demo

[Live Demo](https://will123195.github.io/venti/demo/) and view [source code for demo app](https://github.com/will123195/venti/tree/master/demo/src).

```
npm run demo
```

## Usage

```jsx
import React from 'react'
import { useVenti, state } from 'venti'

const randomize = () => state.set('random', Math.random())

export default function RandomButtonComponent() {
  const state = useVenti()
  const random = state.get('random')
  return <button onClick={randomize}>{random}</button>
}
```

## API

### `useVenti()`
  - Returns `state` 
  - See [StateEventer](https://github.com/will123195/state-eventer) for more info

### `state.get( path, [defaultValue] )`
  - `path` {Array|string} The path to get
  - `defaultValue` {*} (optional) The value returned for undefined resolved values
  - Returns the resolved value

### `state.set( path, value )`
  - `path` {Array|string} The path of the property to set
  - `value` {*} The value to set

### `state.unset( path )`
  - `path` {Array|string} The path of the property to unset

## Tests

```
npm test
```

## License

MIT