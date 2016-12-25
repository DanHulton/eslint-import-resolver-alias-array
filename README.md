# eslint-import-resolver-alias

This is a simple Node module import resolution plugin for [`eslint-plugin-import`](https://www.npmjs.com/package/eslint-plugin-import), which supports module alias.

## Example

```js
module.exports = {
  settings: {
    'import/resolver': {
      'alias': [
        ['babel-polyfill', 'babel-polyfill/dist/polyfill.min.js'],
        ['material-ui/DatePicker', '../custom/DatePicker'],
        ['material-ui', 'material-ui-ie10']
      ]
    }
  }
};
```


Note:

- The items of alias config array is also array which contains 2 string
    + The first string represents the mapped module
    + The second string represents the module alias
- The order of 'material-ui/DatePicker' and 'material-ui' cannot be reversed, otherwise the alias rule 'material-ui/DatePicker' does not work.

## CHANGELOG

[`CHANGELOG`](./CHANGELOG.md)

## References:

- eslint-plugin-import/no-extraneous-dependencies
- eslint-plugin-import/no-unresolved
- eslint-module-utils/resolve
- resolve
- eslint-import-resolver-node