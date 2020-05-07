# yarn-bug-repro

```
git clone git@github.com:bertho-zero/yarn-bug-repro.git
cd yarn-bug-repro/packages/package-1
yarn start
```

result:

```
internal/modules/cjs/loader.js:985
  throw err;
  ^

Error: Cannot find module 'w3c-xmlserializer/lib/XMLSerializer'
Require stack:
- /home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/jsdom/living/index.js
- /home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/jsdom/browser/Window.js
- /home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/api.js
- /home/bertho/dev/yarn-bug-repro/packages/package-1/bug.js
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:982:15)
    at Function.Module._load (internal/modules/cjs/loader.js:864:27)
    at Module.require (internal/modules/cjs/loader.js:1044:19)
    at require (internal/modules/cjs/helpers.js:77:18)
    at Object.<anonymous> (/home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/jsdom/living/index.js:66:25)
    at Module._compile (internal/modules/cjs/loader.js:1158:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1178:10)
    at Module.load (internal/modules/cjs/loader.js:1002:32)
    at Function.Module._load (internal/modules/cjs/loader.js:901:14)
    at Module.require (internal/modules/cjs/loader.js:1044:19) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    '/home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/jsdom/living/index.js',
    '/home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/jsdom/browser/Window.js',
    '/home/bertho/dev/yarn-bug-repro/node_modules/jsdom/lib/api.js',
    '/home/bertho/dev/yarn-bug-repro/packages/package-1/bug.js'
  ]
}
```
