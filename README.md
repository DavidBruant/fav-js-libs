# List of JavaScript libraries i use and recommend

List curated by David Bruant

## Client-side applications

### [Svelte](https://svelte.dev/)

Svelte is a library that enables to create and compose UI components

I've had a lot of experience with preact/React, a little with Vue and vanilla JS (JavaScript with no framework) and my favorite dev experience has ben with Svelte

### [baredux](https://github.com/DavidBruant/baredux)

It's a state-management library that i have authored.

It's inspired by redux, vuex and rematch and is simpler than all that. It's 1 file of ~70 lines of code and will probably never get bigger than 100 lines

### [page.js](https://github.com/visionmedia/page.js)

a client-side routing library

I'm more comfortable with a dedicated client-side library that takes care of routing than the approaches à la react-router which makes routes as components


## Client-side helper libraries

### [d3-fetch](https://github.com/d3/d3-fetch)

A little known fact about [d3](https://d3js.org/) is that its parts can be used as independent modules

i love d3-fetch, because it's the fetch that should have been the browser fetch.\
While the [browser `fetch`](https://developer.mozilla.org/en-US/docs/Web/API/GlobalFetch/fetch) requires two `.then()` to get to your result, d3.fetch gets to the point directly:

```js
fetch(url)
.then(resp => resp.json())
.then(data => console.log(data))

// compared to
import {json} from 'd3-fetch'

json(url)
.then(data => console.log(data))
```

d3-fetch also has the good idea to consider HTTP 4xx and 5xx responses as errors caught via `.catch()` while browser `fetch` considers them "successes" to be handled manually after a first `.then()`


## Tests

### [ava](https://github.com/avajs/ava)

I've had experience with mocha and jest and i prefer ava


## Tooling

### [Rollup](rollupjs.org/)

Rollup is a JS bundler. It works fine for me (and is sort of compulsory with svelte anyway).\
I used browserify for a while


### [npm-run-all](https://www.npmjs.com/package/npm-run-all)

This is a great way to compose [npm run scripts](https://docs.npmjs.com/cli/v7/commands/npm-run-script/) so they run in sequence or in parallel


### [sass](https://www.npmjs.com/package/sass)

My favorite way to write CSS is to write SCSS (which is part of the Sass project)

[node-sass](https://npmjs.org/package/node-sass) is [deprecated](https://sass-lang.com/blog/libsass-is-deprecated)
