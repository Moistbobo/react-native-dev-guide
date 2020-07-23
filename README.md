# Project Initialization Guide

## React
Dependencies

` yarn add react-router-dom redux redux-saga reselect moment typesafe-actions`

devDependencies
`yarn add --dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-recommended eslint-config-typescript eslint-plugin-prettier eslint-plugin-react prettier  eslint-config-esnext eslint-plugin-babel",
`

.eslintrc.js
```
module.exports = {
	parser: '@typescript-eslint/parser',
	extends: [
		'esnext',
		'esnext/style-guide',
		'plugin:react/recommended',
	],
	plugins: [
		'@typescript-eslint',
	],
	rules: {
		'sort-imports': 0, // sorts imports alphabetically but does not auto fix. disabled as import order may matter for some modules
		'no-unused-vars': 0, // disabled in favor of typescript rule @typescript-eslint/no-unused-vars
		'react/jsx-filename-extension': [ 1, { extensions: [ '.jsx', '.tsx' ] } ], // only allow jsx in .jsx and .tsx files
		'no-underscore-dangle': 0, // disabled as it may sometimes be necessary to use _ to denote scoped variabled
		'no-extra-semi': 0, // allow extra semicolon at the end of a statement
		semi: 0, // allow extra semicolon at the end of a statement
		'no-use-before-define': 0, // disabled as we declare styles after component declaration
		'no-console': 'warn', // flag console logs so they are easier to find and remove when pushing to production
		'react-native/no-color-literals': 0, // allow inline color
		'import/named': 0, // disabled due to conflicts with dependencies
		'import/namespace': 0, // disabled due to conflicts with dependencies
		'import/no-namespace': 0, // disabled due to conflicts with dependencies
		'import/default': 0, // disabled due to conflicts with dependencies
		'import/no-named-as-default': 0, // disabled due to conflicts with dependencies
		'import/no-named-as-default-member': 0, // disabled due to conflicts with dependencies
		'import/no-unresolved': 0, // causes issues with MyTypes
		'import/extensions': 0, // disabled due to conflicts with dependencies
		'@typescript-eslint/no-use-before-define': 0, // disabled as we declare styles after component declaration
		'@typescript-eslint/interface-name-prefix': 0, // adhere to c++/java conventions
		'@typescript-eslint/explicit-function-return-type': 0, // disabled as it makes mapDispatchToProps definitions unnecessarily complex
		'@typescript-eslint/explicit-member-accessibility': 0, // disabled as data types used in the app do not require this abstraction
		'@typescript-eslint/no-unused-vars': 'error', // Flag all unused imports as errors
		'react/display-name': 0, // unnecessary for react-native applications
		'react-hooks/exhaustive-deps': 0, // disabled as there are cases where you don't require exhaustive deps
		'no-nested-ternary': 'error', // enabled as nested ternary operators are can be hard to read and debug
		'no-invalid-this': 0, // disabled as it interferes with this.setState calls
		'class-methods-use-this': 0, // interferes with class component function usage
		'import/no-commonjs': 0, // interferes with asset imports
		'no-alert': 0, // need to be able to show alerts
		'no-undef': 0, // interferes with global calls
		'no-extra-parens': 0, // sometimes extra parenthesis keeps code organized
	},
	env: {
		es6: true,
		jest: true,
	},
	globals: {
		window: true,
		fetch: false,
	},
	settings: {
		'import/resolver': {
			node: {
				extensions: [ '.js', '.jsx', '.ts', '.tsx', '.json' ],
			},
		},
	},
};

```
