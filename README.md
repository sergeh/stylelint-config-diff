# stylelint-config-shopify
[![Circle CI](https://circleci.com/gh/sergeh/stylelint-config-diff.svg?style=shield)](https://circleci.com/gh/sergeh/stylelint-config-diff)
[![David-DM](https://david-dm.org/sergeh/stylelint-config-diff.svg)](https://david-dm.org/sergeh/stylelint-config-diff)

Diff's stylelint rules and config

## Installation

Install [stylelint](https://stylelint.io/) and `stylelint-config-shopify`:

**With Yarn**
```
yarn add --dev stylelint sergeh/stylelint-config-diff#master
```

**With npm**
```
npm install stylelint sergeh/stylelint-config-diff#master --save-dev
```


## Usage
Diff's stylelint rules come bundled in `stylelint-config-diff`. To enable these rules, add a `stylelint` property in your `package.json`. See the [stylelint configuration docs](https://stylelint.io/user-guide/configuration/) for more details.
```
"stylelint": {
  "extends": ["stylelint-config-diff"]
}
```

Now you can run stylelint by adding the following linting script to your `package.json`. See the [stylelint CLI docs](https://stylelint.io/user-guide/cli/) for more details.
```
"scripts": {
  "stylelint": "stylelint 'src/**/*.scss'"
}
```
Run it:

**With Yarn**
```
yarn run stylelint
```

**With npm**
```
npm run stylelint
```

## Prettier

This config also includes a prettier config which can be extended to format `.scss`.
Using the [`stylelint-prettier`](https://github.com/bpscott/stylelint-prettier) plugin, prettier changes are exposed as stylelint rule violations.

Install [`prettier`](https://github.com/prettier/prettier):

```
$ yarn add --dev prettier
```

Extend the config in your `package.json`:

```json
"stylelint": {
  "extends": [
    "stylelint-config-diff/prettier"
  ]
}
```

Add a prettier config in `package.json`:

```json
"prettier": {
  "singleQuote": true,
  "trailingComma": "es5",
  "bracketSpacing": false
}
```

Prettier fixes shall be reported when you run `stylelint **/*.css` and shall be autofixed when you run `stylelint --fix **/*.scss`.
