![](https://www.sealights.io/wp-content/uploads/2017/11/code_quality.png)

# Javascript Style Guide

The purpose of this is to:

1. **Enforce** best practices
2. **Improve** code consistency and readability
3. **Ease** projects maintenance amongst different teams and workgroups

Conversations and contributions are welcome!  
Some rules can be disputed, so the voice of everyone who writes JS code will be heard.


## How to use

### 1. Set rules

Put **.eslintrc.json** from this repo to the root of your project

### 2. Install ESLint as dependency

```
npm install --save-dev \
  eslint \
  eslint-plugin-react \
  eslint-plugin-import \
  eslint-plugin-promise \
  eslint-import-resolver-webpack
```

### 3. Install ESLint extension

#### Visual Studio Code

 - Ctrl + Shift + X
 - Search ESLint
 - Install ESLint
 - Restart editor

#### Sublime Text

*(via [Package Control](https://packagecontrol.io/))*
 - Ctrl + Shift + P
 - type Install Package
 - type ESLint
 - Enter
 - Restart editor

#### WebStorm

[See "Using JavaScript Code Quality Tools" section in official docs](https://www.jetbrains.com/help/webstorm/2016.1/using-javascript-code-quality-tools.html?origin=old_help#installESLint).

### 4. Behold!

Now problematic code will be highlighted (specifying which rule is violated).  
*For VSCode you may want to make highlights less bright, see 
[this answer](https://stackoverflow.com/questions/43454967/disable-wavy-underline-in-vs-code/48610661#48610661).*

![screenshot](https://code.visualstudio.com/assets/docs/nodejs/reactjs/app-is-unused.png)

## How to fix automatically

```
eslint --fix filename.js
```

This works for most of codestyle-related rules.  
Also there is an "autofix on save" setting available for VSCode and Sublime.


## How to ignore false-positive rules

For whole current file:
```
/* eslint-disable no-multi-spaces */
```

For specific function: 
```
function someFunction (someParams) { // eslint-disable-line complexity
  ...
}
```


## Rules lists

All rules contain descriptions and examples:

- [ES6](https://eslint.org/docs/rules/)
- [React](https://www.npmjs.com/package/eslint-plugin-react#list-of-supported-rules)
- [Promises](https://www.npmjs.com/package/eslint-plugin-promise#rules)
- [Imports](https://www.npmjs.com/package/eslint-plugin-import#rules)
