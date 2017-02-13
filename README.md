# KSS ♥ brunch.io

[![npm](https://img.shields.io/npm/v/kssbrunch.svg)](https://www.npmjs.com/package/kssbrunch)
[![Travis](https://img.shields.io/travis/FaKeller/kss-brunch.svg)](https://github.com/FaKeller/kss-brunch)
[![npm](https://img.shields.io/npm/l/kssbrunch.svg)](https://www.npmjs.com/package/kssbrunch)

Integrates the [kss-node](https://github.com/kss-node/kss-node) living styleguide generator into your [brunch.io](http://brunch.io/) builds.

The plugin will generate the KSS node styleguide into `<public>/styleguide`.


## Usage

Install the plugin via npm with `npm install --save-dev kssbrunch` or `yarn add kssbrunch -D`.


## Options

Put all options for this plugin into the `config.plugins.kss` object, for example:


```javascript
// file: brunch-config.js

module.exports = {
  plugins: {
    kss: {
      // include generated CSS files in the KSS styleguide. Defaults to true. 
      addCssFiles: true,
      // include generated JS files in the KSS styleguide. Defaults to true.
      addJsFiles: false,
      
      // kss-node specific config
      kssConfig: {
        // will be passed to kss-node
      }
    }
  }
};
```

See all possible options for the `kssConfig` object in the [kss-node documentation](https://github.com/kss-node/kss-node#using-the-command-line-tool).

### Automatic KSS Config for CSS/JS Files

While the `kssConfig` options are passed to kss-node, parts of it are automatically generated by the plugin.
The `kssConfig.css` and `kssConfig.js` options define a set of files paths that are included from the generated living styleguide document.
kssbrunch automatically adds all CSS/JS files generated by brunch to those config options.

> Note: In case you manually set the options in the brunch plugin config, kssbrunch will merge those with the files generated by brunch. 

## Contributing

Open a PR :-)


## [Change Log](CHANGELOG.md)

See all changes made to this project in the [change log](CHANGELOG.md). This project follows [semantic versioning](http://semver.org/).


## [License](LICENSE)

This project is licensed under the terms of the [MIT license](LICENSE).


---

Project created and maintained by [Fabian Keller](http://www.fabian-keller.de).
