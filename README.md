@alasdair/karma-scss-preprocessor
=======================

[![Latest Stable Version](https://img.shields.io/npm/v/karma-scss-preprocessor.svg)](https://www.npmjs.com/package/@alasdair/karma-scss-preprocessor)
[![License](https://img.shields.io/npm/l/karma-scss-preprocessor.svg)](https://www.npmjs.com/package/@alasdair/karma-scss-preprocessor)
[![NPM Downloads](https://img.shields.io/npm/dm/karma-scss-preprocessor.svg)](https://www.npmjs.com/package/@alasdair/karma-scss-preprocessor)
[![dependencies Status](https://david-dm.org/amercier/karma-scss-preprocessor/status.svg)](https://david-dm.org/alasdairhurst/karma-scss-preprocessor)
[![devDependencies Status](https://david-dm.org/amercier/karma-scss-preprocessor/dev-status.svg)](https://david-dm.org/alasdairhurst/karma-scss-preprocessor?type=dev)
[![peerDependencies Status](https://david-dm.org/amercier/karma-scss-preprocessor/peer-status.svg)](https://david-dm.org/alasdairhurst/karma-scss-preprocessor?type=peer)

> Karma preprocessor to compile Sass files on the fly with [sass](https://www.npmjs.com/package/sass).
> In contrast of [karma-sass-preprocessor](https://www.npmjs.com/package/karma-sass-preprocessor),
> it does not write any intermediate file to the disk, and does not use any
> [Gulp](http://gulpjs.com/) plugin.

Installation
------------

```bash
npm install @alasdair/karma-scss-preprocessor sass --save-dev
```

This is a fork of karma-scss-preprocessor. The main difference is that `sass` is used instead of `node-sass`.

Note: since v5.0, [sass](https://www.npmjs.com/package/sass) is used
as a [peer dependency](https://docs.npmjs.com/files/package.json#peerdependencies).
That is why you need to install it along with this module.

Configuration
-------------

See [sass options](https://www.npmjs.com/package/sass) for more
details.

```js
module.exports = function (config) {
  config.set({
    preprocessors: {
      'src/**/*.scss': ['scss']
    },
    scssPreprocessor: {
      options: {
        sourceMap: true,
        includePaths: ['bower_components']
      }
    }
  });
};
```
