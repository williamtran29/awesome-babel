# Awesome Babel [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

[<img src="https://babeljs.io/images/logo.svg" width="160" align="right" alt="babel">](http://babeljs.io)

> A list of awesome Babel plugins, presets, etc. Many of these are from the community, but some are lesser-known
> plugins in the Babel organization that may be useful to you.

> As always, use caution when trying out Babel plugins, especially those marked as 🔧 *experimental* or 🔧🚧 *under construction*.

If you want to contribute, please read the [contribution guidelines](contributing.md).

## Parsers

 - [babel-eslint](https://github.com/babel/babel-eslint) - ESLint using Babel as the parser.
   - Note: ESLint now lints most ES6+ syntax. This parser is only necessary if you are using Flow types or other experimental features.

## Plugins

### General Plugins

 - [external-helpers](https://www.npmjs.com/package/babel-plugin-external-helpers) - Moves helper functions to a single imported module.
 - [fast-async](https://github.com/MatAtBread/fast-async) - Uses nodent to compile async/await to fast Promise output.
 - [feature-flags](https://github.com/ember-cli/babel-plugin-feature-flags) - Helper for managing application feature flags.
 - [idx](https://github.com/facebookincubator/idx) - library + babel plugin for a existential function.
 - [transform-builtin-extend](https://github.com/loganfsmyth/babel-plugin-transform-builtin-extend) - Enable extending builtin types like `Error` and `Array`, which require special treatment and require static analysis to detect.

### Module Resolution

 - [lodash](https://github.com/lodash/babel-plugin-lodash) - Cherry-picks Lodash modules so you don’t have to.
 - [ramda](https://github.com/megawac/babel-plugin-ramda) - Cherry-picks Ramda modules so you don’t have to.
 - [module-resolver](https://github.com/tleunen/babel-plugin-module-resolver) - Custom module resolver.
 - [root-import](https://github.com/entwicklerstube/babel-plugin-root-import) - Import modules from the root with `require('~/foo')` syntax.
 - [webpack-alias](https://github.com/trayio/babel-plugin-webpack-alias) - Allows you to use webpack aliases and most of webpack resolve features in Babel.

### React

 - [React Optimize](https://github.com/thejameskyle/babel-react-optimize) - A Babel preset and plugins for optimizing React code.
 - [React Transform](https://github.com/gaearon/babel-plugin-react-transform) - Instrument React components with custom transforms.
 - [react-docgen](https://github.com/kadirahq/babel-plugin-react-docgen) - Makes propTypes comments accessible at runtime for use with documentation generators.
 - [react-require](https://github.com/vslinko/babel-plugin-react-require) - Adds React import declaration if file contains JSX tags.
 - [transform-react-remove-prop-types](https://github.com/oliviertassinari/babel-plugin-transform-react-remove-prop-types) - Removes unnecessary React propTypes from the production build.
 - [transform-react-jsx-self](https://github.com/babel/babel/tree/master/packages/babel-plugin-transform-react-jsx-self) - Adds a `__self` property to JSX tags for debugging. Don't use in production. [More info](https://github.com/babel/babel/pull/3540)
 - [transform-react-constant-elements](https://www.npmjs.com/package/babel-plugin-transform-react-constant-elements) - Hoist elements that can be marked as constant to the highest scope for reuse.
 - [transform-react-inline-elements](https://www.npmjs.com/package/babel-plugin-transform-react-inline-elements) - Replaces `React.createElement()` with a helper that is more optimized for production.
 - [react-hyperscript](https://github.com/roman01la/babel-plugin-react-hyperscript) - HyperScript syntax for React components without runtime overhead.

### Internationalization

 - [c-3po](https://c-3po.js.org) - Localization tool based on es6 template literals.
 - [react-intl](https://github.com/yahoo/react-intl) - Extracts string messages for translation from modules that use [React Intl](https://github.com/yahoo/react-intl).

### Types

 - [flow-runtime](https://github.com/codemix/flow-runtime/tree/master/packages/babel-plugin-flow-runtime) - Turns Flow annotations into runtime checks. Part of [Flow-Runtime](https://codemix.github.io/flow-runtime).
 - [tcomb](https://github.com/gcanti/babel-plugin-tcomb) - Turns Flow annotations into typechecks with [tcomb](https://github.com/gcanti/tcomb).
 - [jsdoc-to-assert](https://github.com/azu/babel-plugin-jsdoc-to-assert) - Turns JSDoc into runtime checks.
 - [runtyper](https://github.com/vitalets/babel-plugin-runtyper) - Detects type-mismatch operations in runtime without annotations.

### Testing

 - [espower](https://github.com/power-assert-js/babel-plugin-espower) - Annotates call sites for descriptive messages when using [power-assert](https://github.com/power-assert-js/power-assert).
 - [istanbul](https://github.com/istanbuljs/babel-plugin-istanbul) - Instruments your code with Istanbul coverage.
 - [rewire](https://github.com/speedskater/babel-plugin-rewire) - Adds the ability to rewire module dependencies. This enables to mock modules for testing purposes.

### Optimization

 - [groundskeeper-willie](https://github.com/betaorbust/babel-plugin-groundskeeper-willie) - Removes debugger and console calls.
 - [loop-optimizer](https://github.com/vihanb/babel-plugin-loop-optimizer) - Transforms `.forEach` and `.map` calls to for loops. 🔧
 - [closure-elimination](https://github.com/codemix/babel-plugin-closure-elimination) - Transforms closures into separate functions.

### Syntax Sugar

 - [implicit-return](https://github.com/miraks/babel-plugin-implicit-return) - Transforms last statement in a function block to a return statement.
 - [transform-iota](https://github.com/passcod/babel-plugin-transform-iota) - Golang-style `iota()`. 🔧
 - [offside-js](https://github.com/shanewholloway/babel-plugin-offside-js) - Coffeescript-like indented block syntax hack. 🔧🚧
 - [trace](https://github.com/codemix/babel-plugin-trace) - Syntax shortcuts for console logging.
 - [meaningful-logs](https://github.com/furstenheim/babel-plugin-meaningful-logs) - Adds file name and line number of caller to `console.log()` calls.

### Alternative Programming Paradigms

 - [macros](https://github.com/codemix/babel-plugin-macros) - Hygienic, non-syntactic macros.
 - [contracts](https://github.com/codemix/babel-plugin-contracts) - Design by Contract; Includes preconditions, postconditions, and invariant conditions.
 - [transform-scala-lambda](https://github.com/xtuc/babel-plugin-transform-scala-lambda) - Enable Scala-style lambdas (using `_`). 🔧
 - [partial-application](https://github.com/citycide/babel-plugin-partial-application) - Scala/Kotlin-esque partial application syntax for JavaScript (using `_`). 🔧
 - [overload](https://github.com/foxbenjaminfox/babel-plugin-overload) - Allow overloading default operators like `+` or `===` for specific classes. 🔧🚧

## Presets

 - [env](https://github.com/babel/babel-preset-env) - **The recommended preset** which includes transforms based on the specified environment (browsers, node, electron, etc).
 - [React](https://www.npmjs.com/package/babel-preset-react) - Babel preset for all React plugins.
 - [React Optimize](https://github.com/thejameskyle/babel-react-optimize) - A Babel preset and plugins for optimizing React code.

## Tooling

 - [babel-watch](https://github.com/kmagiera/babel-watch) - Reloads a node app on file changes.


## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
