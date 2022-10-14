# esbuild-spreadbug-example

## Steps to reproduce

```bash
npm install
npm run build
npm run start
```

### Expected Output

```bash
{ propA: "valueA" }
```

### Actual Output

```bash
> esbuild-spreadbug-example@1.0.0 start /Users/me/code/esbuild-spreadbug-example
> node dist/main.js

/Users/me/code/esbuild-spreadbug-example/dist/main.js:8
  for (var prop in b2 ||= {})
                        ^

SyntaxError: Unexpected token '='
    at Object.compileFunction (vm.js:344:18)
    at wrapSafe (internal/modules/cjs/loader.js:1048:15)
    at Module._compile (internal/modules/cjs/loader.js:1082:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1138:10)
    at Module.load (internal/modules/cjs/loader.js:982:32)
    at Function.Module._load (internal/modules/cjs/loader.js:875:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:71:12)
    at internal/main/run_main_module.js:17:47
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! esbuild-spreadbug-example@1.0.0 start: `node dist/main.js`
npm ERR! Exit status 1
```
