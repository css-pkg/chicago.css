# chicago.css

ChicagoFLF font as a node packaged module.

[![latest version][npm-img]][npm-url] [![build status][travis-img]][travis-url] [![stability][stability-img]][stability-url] [![downloads][downloads-img]][npm-url]

[npm-img]: https://img.shields.io/npm/v/chicago.css.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/chicago.css
[travis-img]: https://img.shields.io/travis/bcomnes/chicago.css.svg?style=flat-square
[travis-url]: https://travis-ci.org/bcomnes/chicago.css
[stability-img]: https://img.shields.io/badge/stability-stable-brightgreen.svg?style=flat-square
[stability-url]: https://iojs.org/api/documentation.html#documentation_stability_index
[downloads-img]: https://img.shields.io/npm/dm/chicago.css.svg?style=flat-square

## Install

```sh
# npm package
$ npm install chicago.css
```

The css is exported from the package.json main field and can be imported using a css bundler or copied out of `node_modules` as part of a larger build process.

## Usage

```css
@import 'chicago.css';

body { font-family: ChigacoFLF, sans-serif; }
```

### PostCSS

You can use PostCSS to inline and import this css module using the following `postcss.config.js`:

```js
module.exports = (ctx) => ({
  plugins: {
    'postcss-import': { root: ctx.file.dirname }, // Inline module css
    'postcss-url': { // Copy assets from node_modules
      url: 'copy',
      useHash: true,
      assetsPath: 'assets'
    }
  }
})
```

```
$ postcss styles.css -o dist/bundle.css
```
- [postcss/postcss](https://ghub.io/postcss)
- [jantimon/postcss-inline](https://github.com/jantimon/postcss-inline)
- [postcss/postcss-url](https://github.com/postcss/postcss-url)

## Credits

- [christtrekker.users.sourceforge.net/fnt/chicago.shtml](http://christtrekker.users.sourceforge.net/fnt/chicago.shtml)
- [en.wikipedia.org/wiki/Chicago_(typeface)](https://en.wikipedia.org/wiki/Chicago_(typeface))

## See also

- [style.css](https://github.com/ungoldman/style.css)
- [top-bar.css](https://github.com/ungoldman/top-bar.css)
- [fraktur.css](https://github.com/bcomnes/fraktur.css)
- [go-fonts.css](https://github.com/bcomnes/go-fonts.css)
