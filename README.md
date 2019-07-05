# vue-banana-i18n

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/master/LICENSE) [![npm version](https://img.shields.io/npm/v/vue-banana-i18n.svg?style=flat)](https://www.npmjs.com/package/vue-banana-i18n) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://reactjs.org/docs/how-to-contribute.html#your-first-pull-request)

A [banana-i18n](https://github.com/wikimedia/banana-i18n) wrapper to support localization in Vue.js

[Playground](https://codepen.io/santhoshtr/pen/YoOzEM)

## Installation

```javascript
npm install vue-banana-i18n
```

then

```javascript
import i18n from 'vue-banana-i18n'
```

## Basic Usage

``` html
<div id="app">
  <h1>{{ $i18n('hello_world') }}</h1>
  <h2 class='result'>{{ $i18n('search_results', 10) }}</h2>
  <div class='status'>{{ $i18n('profile_change_message', 'Alice', 'female') }}</h2>
</div>

```

``` javascript
import Vue from 'vue'
import i18n from 'vue-banana-i18n'

const messages = {
  en: {
    'hello_world': 'Hello world',
    'search_results': 'Found $1 {{PLURAL:$1|result|results}}',
    'profile_change_message': '$1 changed {{GENDER:$2|his|her}} profile picture'
  },
  ml: {
    'hello_world': 'എല്ലാവർക്കും നമസ്കാരം',
    'search_results': '{{PLURAL:$1|$1 ഫലം|$1 ഫലങ്ങൾ|1=ഒരു ഫലം}} കണ്ടെത്തി',
    'profile_change_message': '$1 {{GENDER:$2|അവന്റെ|അവളുടെ}} പ്രൊഫൈൽ പടം മാറ്റി'
  }
}

Vue.use(i18n, {
  locale:'es',
  messages:messages
})
```

## Message format

The Banana i18n system and its messages are documented at [banana-i18n](https://github.com/wikimedia/banana-i18n)

## License:

[MIT](https://cos.mit-license.org/)