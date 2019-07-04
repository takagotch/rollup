### rollup
---
https://github.com/rollup/rollup

```sh
rollup main.js --format iife --name "myBundle" --file bundle.js
rollup main.js --format cjs --file bundle.js
rollup main.js --format umd --name "myBundle" --file bundle.js

rollup main.js --file bundle.js --format iife
rollup main.js --file bundle.js --format cjs
rollup main.js --file bundle.js --format umd --name "myBundle"
```

```js
var utils = require( 'utils' );
var query = 'Rollup';
utils.ajax( 'https://api.example.com?search=' + query ).then( handleResponse );

import { ajax } from 'utils';
var query = 'Rollup';
ajax( 'https://api.example.com?search=' + query ).then( handleResponse );

const utils = require( './utils' );
const query = 'Rollup';
utils.ajax('https://api.example.com?search=${query}').then(handleResponse);

import { ajax } from './utils';
const query = 'Rollup';
ajax('https://api.example.com?search=${query}').then(handleResponse);

module.exports = {
  input: 'src/main.js',
  output: {
    file: 'bundle.js',
    format: 'cjs'
  }
};

// rollup.config.js
export default {
  input,
  external,
  plugins,
  owwarn,
  perf,
  acorn,
  acornInjectPlugins,
  treeshake,
  context,
  moduleContext,
  experimentalCodeSplitting,
  manualChunks,
  optimizeChunks,
  chunkGroupingSize,
  output: {
    format,
    file,
    dir,
    name,
    globals,
    paths,
    banner,
    footer,
    intro,
    outro,
    sourcemap,
    sourcemapFile,
    sourcemapPathTransform,
    interop,
    extend,
    exports,
    amd,
    indent,
    strict,
    freeze,
    namespaceToStringTag,
    entryFileNames,
    chunkFileNames,
    assetFileNames
  },
  watch: {
    chokidar,
    include,
    exclude,
    clearScreen
  }
}

// rollup.config.js
export default [{
  input: 'main-a.js',
  output: {
    file: 'dist/bundle-a.js',
    format: 'cjs'
  }
}, {
  input: 'main-b.js',
  output: [
    {
      file: 'dist/bundle-b1.js',
      format: 'cjs'
    },
    {
      file: 'dist/bundle-b1.js',
      format: 'cjs'
    },
    {
      file: 'dist/bundle-b2.js',
      format: 'esm'
    }
  ]
}];

import fetch from 'node-fetch';
export default fetch('/some-remote-service-or-file-which-returns-actual-config');

export default Promise.all([
  fetch('get-config-1'),
  fetch('get-config-2')
])

import defaultConfig form './rollup.default.config.js';
import debugConfig from './rollup.debug.config.js';

export default commandLineArgs => {
  if(commandLineArgs.configDebug === true){
    return debugConfig;
  }
  return defaltConfig;
}

const rollup = require('rollup');
const inputOptions = {...};
const outputOptions = {...};

async function build(){
  const bundle = await rollup.rollup(inputOptions);
  console.log(bundle.imports);
  console.log(bundle.exports);
  console.log(bundle.modules);
  const { code, map } = await bundle.generate(outputOptions);
  await bundle.write(outputOptions);
}
bundle();

const inputOptions = {
  input,
  external,
  plugins,
  onwarn,
  cache,
  perf,
  acorn,
  acornInjectPlugins,
  treeshake,
  context,
  moduleContext,
  experimentalCodeSplitting,
  manualChunks,
  optimizeChunks,
  chunkGroupingSize
}

const rollup = require('rollup');
const watchOptions = {};
const watcher = rollup.watch(watchOptions);
watcher.on('event', event => {
  // event.code can be one of:
});
watcher.close();
```

```js
// rollup.config.js
export default{
  watch:{
    include: 'src/**'
  }
};

export default {
  watch: {
    exclude: 'node_module/**'
  }
};
```
