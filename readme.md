# Mocha Sidebar Excludes Ignored Error

Error reproduction example for [mocha-sidebar#155](https://github.com/maty21/mocha-sidebar/issues/155).

## Steps to Reproduce Error From This Repository

1. run `npm install`

2. Run the tests in debug mode from mocha sidebar. When this is done one of the `*.spec.js` files in `node_modules` should throw since it wasn't excluded as the `mocha.files.ignore` says it should be. The tests in `node_modules` normally throw, because their devDependencies have not been downloaded.

3. Run the tests without debug mode and notice how the node_modules files are properly excluded as given by `mocha.files.ignore`.
