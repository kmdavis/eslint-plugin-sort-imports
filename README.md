# eslint-plugin-sort-imports-es6-autofix

A sort-imports rule that properly distinguishes between ES6 import types.

It accepts the same options as the [original rule](http://eslint.org/docs/rules/sort-imports), but the `multiple` type corresponds to all named imports (regardless of how many are imported), while the `single` type corresponds only to default imports, and adds a `combined` type that mixes `all`, `multiple`, and `single` imports and alphabetizes them together.

This rule respects whitespace and comments between imports by only looking at the order of (and sorting) consecutive import statements (those without newlines/comments in between them).

## Usage

`npm i --save-dev eslint-plugin-sort-imports-es6-autofix`

```json
{
  "plugins": [
    "@kmdavis/sort-imports"
  ],
  "rules": {
    "@kmdavis/sort-imports/sort-imports": [2, {
      "ignoreCase": false,
      "ignoreMemberSort": false,
      "memberSyntaxSortOrder": ["combined", "none"]
    }]
  }
}
```
