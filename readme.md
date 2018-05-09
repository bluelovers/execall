# execall [![Build Status](https://travis-ci.org/sindresorhus/execall.svg?branch=master)](https://travis-ci.org/sindresorhus/execall)

> Find multiple RegExp matches in a string

Instead of having to iterate over `RegExp#exec`, immutable, and with a nicer result format.


## Install

```nodemon
$ npm install execall2
```

## Usage

```ts
import execall from 'execall2';
import * as execall from 'execall2';
import { execall } from 'execall2';
const execall = require('execall2');
```

```ts
let t = execall(/(?<k>.)/g, '123456789');
```

```ts
[ [ '1', '1', index: 0, groups: { k: '1' }, match: '1', sub: [ '1' ] ],
  [ '2', '2', index: 1, groups: { k: '2' }, match: '2', sub: [ '2' ] ],
  [ '3', '3', index: 2, groups: { k: '3' }, match: '3', sub: [ '3' ] ],
  [ '4', '4', index: 3, groups: { k: '4' }, match: '4', sub: [ '4' ] ],
  [ '5', '5', index: 4, groups: { k: '5' }, match: '5', sub: [ '5' ] ],
  [ '6', '6', index: 5, groups: { k: '6' }, match: '6', sub: [ '6' ] ],
  [ '7', '7', index: 6, groups: { k: '7' }, match: '7', sub: [ '7' ] ],
  [ '8', '8', index: 7, groups: { k: '8' }, match: '8', sub: [ '8' ] ],
  [ '9', '9', index: 8, groups: { k: '9' }, match: '9', sub: [ '9' ] ] ]
getOwnPropertyNames [ '0', '1', '2', '3', '4', '5', '6', '7', '8', 'length', 're', 'input' ]
== hidden property ==
{ re: /(?<k>.)/g, input: '123456789' }
```

```ts
execall(/(\d+)/g, '$200 and $400');
/*
[ [ '200',
    '200',
    index: 1,
    groups: undefined,
    match: '200',
    sub: [ '200' ] ],
  [ '400',
    '400',
    index: 10,
    groups: undefined,
    match: '400',
    sub: [ '400' ] ] ]
*/
```


## API

### execall(re, input)

Returns an array of objects with a match, sub-matches, and index.

#### re

Type: `regexp`

Regular expression to match against the `input`.

#### input

Type: `string`


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
