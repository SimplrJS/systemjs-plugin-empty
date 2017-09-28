# systemjs-plugin-empty
SystemJS plugin to ignore files

## Installation
For installing with JSPM:

```
jspm install @plugin-empty=npm:systemjs-plugin-empty
```

For use with SystemJS natively:

```
npm install systemjs-plugin-empty
```

Then add the configuration:

```js
SystemJS.config({
  map: {
     "@plugin-empty": "node_modules/systemjs-plugin-empty/empty.js"
  }
});
```

## Setup
To load with the plugin set:

```js
SystemJS.config({
  meta: {
    "*.css": { loader: "@plugin-empty" },
    "*.ext": { loader: "@plugin-empty" }
  }
});
```

Or via package configuration:

```js
SystemJS.config({
  packages: {
    "src/": {
      meta: {
        "*.css": { loader: "@plugin-empty" },
        "*.ext": { loader: "@plugin-empty" }
      }
    }
  }
});
```

## License
MIT
