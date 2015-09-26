# Laravel Elixir Bower

### Install

```sh
$ npm install laravel-elixir-bower --save-dev
```

### Example

bower.json

```javascript
{
  "name": "laravel",
  "version": "1.0.0",
  "license": "MIT",
  "ignore": [
    "**/.*",
    "node_modules",
    "bower_components",
    "test",
    "tests"
  ],
  "dependencies": {
    "bootstrap": "~3.3.5"
  },
  "overrides": {
    "jquery": {
      "main": [
        "dist/jquery.js"
      ],
      "normalize": {
        "": "*.js"
      }
    },
    "bootstrap": {
      "main": [
        "dist/css/bootstrap.min.css",
        "dist/css/bootstrap.css",
        "dist/js/bootstrap.min.js",
        "dist/js/bootstrap.js",
        "dist/fonts/*"
      ],
      "normalize": {
        "css": "*.css",
        "js": "*.js",
        "fonts": [
          "*.eot",
          "*.svg",
          "*.ttf",
          "*.woff",
          "*.woff2"
        ]
      }
    }
  }
}
```

```javascript
var elixir = require('laravel-elixir');

require('laravel-elixir-bower');

elixir(function (mix) {

    // Bower dependencies
    mix.bower({
        src: './bower_components',
        output: './resources/assets/vendor'
    });
});
```