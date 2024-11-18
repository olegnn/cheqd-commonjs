## Current behavior:

```bash
node .
```
=>
```
Error [ERR_REQUIRE_ESM]: require() of ES Module <..>/node_modules/@cheqd/sdk/build/cjs/index.js from <..>/index.js not supported.
<..>/node_modules/@cheqd/sdk/build/cjs/index.js is treated as an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which declares all .js files in that package scope as ES modules.
Instead either rename <..>/node_modules/@cheqd/sdk/build/cjs/index.js to end in .cjs, change the requiring code to use dynamic import() which is available in all CommonJS modules, or change "type": "module" to "type": "commonjs" in <..>/node_modules/@cheqd/sdk/package.json to treat all .js files as CommonJS (using .mjs for all ES modules instead).
```

## Expected behavior:

The CommonJS module should load and function without any errors.
