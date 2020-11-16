### npm install Issues:

Try running `npm upgrade` before `npm install` to update package.json dependencies.

### Parcel Issues:

Parcel is an ever evolving project that's just getting better. If you run into problems with it not respecting changes (particularly to your `.babelrc` or `.env` files) then delete the `dist/` and the `.cache/` directories. You can do this in bash by running from the root directoy of your project `rm -rf dist/ .cache/` or just by deleting those directories in your editor. This will force Parcel to start over and not cache anything.

### Solution to "regeneratorRuntime is not defined"

The simplest solution is to cut the supported browsers list in your `package.json` file down to:

```js
    "browserslist": [
        "last 2 Chrome versions",
    ]
```

If you run into anything else, open an issue and we'll try to clarify or help!
