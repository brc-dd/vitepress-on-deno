# vitepress-on-deno (issue)

Error:

```
❯ deno task dev       
Warning Currently only basic package.json `scripts` are supported. Programs like `rimraf` or `cross-env` will not work correctly. This will be fixed in an upcoming release.
Task dev deno run -A --unstable --node-modules-dir npm:vitepress dev
error: Uncaught (in promise) BadResource: Bad resource ID
    at Object.isatty (ext:runtime/40_tty.js:19:7)
    at Writable.get [as isTTY] (ext:deno_node/_process/streams.mjs:57:31)
    at createLogger (file:///Users/divyansh/foo/node_modules/.deno/vitepress@1.0.0-beta.1/node_modules/vite/dist/node/chunks/dep-4d3eff22.js:12736:63)
    at file:///Users/divyansh/foo/node_modules/.deno/vitepress@1.0.0-beta.1/node_modules/vitepress/dist/node/cli.js:397:5
    at Object.runMicrotasks (ext:core/01_core.js:836:30)
    at processTicksAndRejections (ext:deno_node/_next_tick.ts:51:14)
    at runNextTicks (ext:deno_node/_next_tick.ts:69:5)
    at eventLoopTick (ext:core/01_core.js:188:21)
```

Temp fix:

Comment out these lines in `cli.js` mentioned above:

<img width="534" alt="image" src="https://github.com/brc-dd/vitepress-on-deno/assets/40380293/7b6a7fb7-e780-451d-82e6-b8c46b8e270c">
