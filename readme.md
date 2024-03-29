## Translo Nodejs

Nodejs client for Translo API

## Import module

```js
const Translo = require('./translo')

const APIKey = 'RAPIDAPI-KEY'
const translo = new Translo(APIKey)
```

## translate

```js
// Promises

translo.translate('Привет, мир!', 'en', 'ru')
.then(response => console.log(response))

// Async

let translate = await translo.translate('Привет, мир!', 'en', 'ru')

```

## batch_translate

```js
// Promises

translo.batchTranslate([
  {"from":"ru","to":"en","text":"Привет, мир!"},
  {"from":"en","to":"ru","text":"Hello, Translo!"}
])
.then(response => console.log(response))

// Async

let batch = await translo.batchTranslate([
  {"from":"ru","to":"en","text":"Привет, мир!"},
  {"from":"en","to":"ru","text":"Hello, Translo!"}
])
```

## detect

```js
// Promises

translo.detect('Translo is the best translator in Telegram')
.then(response => console.log(response))

// Async

let detect = await translo.detect('Translo is the best translator in Telegram')
```
