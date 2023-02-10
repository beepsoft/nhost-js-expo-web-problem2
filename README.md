

When using the `@nhost/nhost-js` (1.13.2) in vanilla React Native Expo 46 or above for web  starting the app fails with an error like this in the web console:

```
wrapNativeSuper.js:31 Uncaught Error: Module parse failed: Unexpected token (285:143)
You may need an appropriate loader to handle this file type, currently no loaders are configured to process this file. See https://webpack.js.org/concepts#loaders
|   };
| }
> const G = typeof window < "u", K = /* @__PURE__ */ new Map(), Pe = (s) => G && typeof localStorage < "u" ? localStorage.getItem(s) : K.get(s) ?? null, Ce = (s, e) => {
|   G && typeof localStorage < "u" ? e ? localStorage.setItem(s, e) : localStorage.removeItem(s) : e ? K.set(s, e) : K.has(s) && K.delete(s);
| }, Ne = (s, e) => {
    at ./node_modules/@nhost/hasura-auth-js/dist/index.esm.js (wrapNativeSuper.js:31:1)
    at __webpack_require__ (bootstrap:789:1)
    at fn (bootstrap:100:1)
    at Module.<anonymous> (index.esm.js:1:1)
    at ./node_modules/@nhost/nhost-js/dist/index.esm.js (index.esm.js:250:1)
    at __webpack_require__ (bootstrap:789:1)
    at fn (bootstrap:100:1)
    at ./App.tsx (App.tsx:1:1)
    at __webpack_require__ (bootstrap:789:1)
    at fn (bootstrap:100:1)
    at ./node_modules/expo/AppEntry.js (AppEntry.js:1:1)
    at __webpack_require__ (bootstrap:789:1)
    at fn (bootstrap:100:1)
    at 1 (log.js:59:1)
    at __webpack_require__ (bootstrap:789:1)
    at bootstrap:856:1
    at bootstrap:856:1
./node_modules/@nhost/hasura-auth-js/dist/index.esm.js	@	wrapNativeSuper.js:31
__webpack_require__	@	bootstrap:789
fn	@	bootstrap:100
(anonymous)	@	index.esm.js:1
./node_modules/@nhost/nhost-js/dist/index.esm.js	@	index.esm.js:250
__webpack_require__	@	bootstrap:789
fn	@	bootstrap:100
./App.tsx	@	App.tsx:1
__webpack_require__	@	bootstrap:789
fn	@	bootstrap:100
./node_modules/expo/AppEntry.js	@	AppEntry.js:1
__webpack_require__	@	bootstrap:789
fn	@	bootstrap:100
1	@	log.js:59
__webpack_require__	@	bootstrap:789
(anonymous)	@	bootstrap:856
(anonymous)	@	bootstrap:856
```

To reproduce the error:

1. yarn
2. yarn web

App startup fails with the error above displayed in the browser's console.

When using 

```
    "expo": "45.0.8",
```

it works, starting from expo 46 it does not. 
