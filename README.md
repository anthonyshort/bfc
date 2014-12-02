# bfc

Make standalone component builds requireable by Browserify. Useful mainly for libraries that are built with Component and want to support npm and Browserify.

```
npm install -g bfc
```

## Usage

```
bfc < ./build/build-standalone.js > ./dist/output.js
```

You can then make `dist/output.js` the `main` field in your package.json and it will require load up just fine.

## This is crappy

Yep. But Browserify parses dependencies for requires and will freak out about not being about to resolve them.

This also means that Browserify builds are requiring the built component rather than the individual components themselves. Generally not too much of a problem if your library is small.