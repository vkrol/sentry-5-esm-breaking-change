# sentry-5-esm-webpack-breaking-change
## Steps
1. Run `npm install` or `yarn`
2. Run `npm run build-and-check-es5` or `yarn build-and-check-es5`
3. Result: everything is OK, `dist/main.js`contains ES5 code only
4. `git checkout upgrade-to-sentry-5`
5. Run `npm run build-and-check-es5` or `yarn build-and-check-es5`
6. Result: `dist/main.js` contains ES6 code
```
ES-Check: there were 1 ES version matching errors.

          ES-Check Error:
          ----
          · erroring file: dist/main.js
          · error: SyntaxError: The keyword 'class' is reserved (125:0)
          · see the printed err.stack below for context
          ----

          SyntaxError: The keyword 'class' is reserved (125:0)
```
