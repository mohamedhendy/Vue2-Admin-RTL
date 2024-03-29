


## Documentation

> [https://devjin0617.gitbooks.io/vue2-admin-lte-guide/](https://devjin0617.gitbooks.io/vue2-admin-lte-guide/)

## Demo Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests: coming soon
# npm run unit

# run e2e tests: coming soon
# npm run e2e

# run all tests: coming soon
# npm test
```

## How to use

First, install `vue2-admin-lte` via npm.

```bash
$ npm i --save vue2-admin-lte
```

append alias config in webpack

```javascript
module.exports = {
  resolve: {
    alias: {
      'va': 'vue2-admin-lte/src'
    }
  }
}
```

import css and javascript files

```javascript
// css files
import 'va/lib/css'

// js files
import 'va/lib/script'
```

use the components in .vue

```vue
<template>
  <va-button
    name="Primary"
    theme="primary"
    size="btn-lg"
    :isFlat="true"
  ></va-button>
</template>

<script>
import VAButton from 'va/components/VAButton.vue'
export default {
  name: 'Button',
  components: {
    'va-button': VAButton
  }
}
</script>
```

## Example

```vue
<template>

  <va-direct-chat
    :talkList="talkList"
    :badgeCount="3"
    theme="primary"
    title="Direct Chat"
    placeholder="Type Messages ..."
  ></va-direct-chat>

</template>


<script>
import VADirectChat from '../path/to/components/VADirectChat.vue'

export default {
  name: 'App',
  data () {
    return {
      talkList: [
        {
          name: 'Alexander Pierce',
          date: new Date(),
          profileImage: 'http://path/to/image',
          message: `Is this template really for free? That's unbelievable`,
          isMine: false
        },
        {
          name: 'Sarah Bullock',
          date: new Date(),
          profileImage: 'http://path/to/image',
          message: `You better believe it!`,
          isMine: true
        }
      ]
    }
  },
  components: {
    'va-direct-chat': VADirectChat
  }
}

</script>
```

## how to start mock server

```javascript
node ./mock-server/index.js
```

## how to use Vuex

```javascript
// /vuex/store.js
import Vue from 'vue'
import Vuex from 'vuex'

import * as actions from './actions'
import * as getters from './getters'
import modules from './modules'

Vue.use(Vuex)

export default new Vuex.Store({
  actions,
  getters,
  modules,
  strict: process.env.NODE_ENV !== 'production'
})
```


## Contributing to Vue2 AdminLTE

The following is a set of guidelines for contributing to `Vue2 AdminLTE`.

### Submitting Issues

You can create an issue [here](https://github.com/devjin0617/vue2-admin-lte/issues).

If you can, please include:
- The version, name of Browser you are using
- The operating system you are using

Other things that will help resolve your issue:
- Screenshots or gif
- dev tools or an alert
- Perform a search to see if a similar issue has already been submitted


### Submitting Pull Requests

- Include screenshots and animated gif in your pull request whenever possible.
- Use short, present tense commit messages.
