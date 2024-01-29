# React & NextJS App Configuration

A feature-rich React & Next.js web application boilerplate with integrated ESLint, Prettier, and Babel.js configurations for seamless code quality and consistency. Speed up your development process and build modern, scalable web apps effortlessly.

## Installation

Create a .eslintrc file or you can clone from my repository. Paste these codes below.

```
{
  "extends": [
    "airbnb",
    "airbnb/hooks",
    "eslint:recommended",
    "prettier",
    "plugin:jsx-a11y/recommended",
    "next/core-web-vitals"
  ],
  "parser": "babel-eslint",
  "parserOptions": {
    "ecmaVersion": 8
  },
  "env": {
    "browser": true,
    "node": true,
    "es6": true,
    "jest": true
  },
  "rules": {
    "react/react-in-jsx-scope": 0,
    "react-hooks/rules-of-hooks": "error",
    "no-console": 0,
    "react/state-in-constructor": 0,
    "indent": 0,
    "linebreak-style": 0,
    "react/prop-types": 0,
    "jsx-a11y/click-events-have-key-events": 0,
    "react/jsx-filename-extension": [
      1,
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "prettier/prettier": [
      "error",
      {
        "trailingComma": "es5",
        "singleQuote": true,
        "printWidth": 100,
        "tabWidth": 4,
        "semi": true,
        "endOfLine": "auto",
        "useTabs": true
      }
    ]
  },
  "plugins": ["prettier", "react", "react-hooks"]
}
```

- For prettier, create `.prettierrc` file in the root directory and paste this code. Required plugin `prettier-plugin-tailwindcss`. Run this command in your terminal `npm i prettier-plugin-tailwindcss` or `yarn add prettier-plugin-tailwindcss` or `pnpm i prettier-plugin-tailwindcss`

```
{
  "trailingComma": "es5",
  "singleQuote": true,
  "printWidth": 100,
  "tabWidth": 4,
  "semi": true,
  "endOfLine": "auto",
  "useTabs": true,
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

- You can use "spaces" instead of "tabs". For you just need to change the value of `"useTabs": false`.

You need configure the the vscode also. Make sure you only configure your `workspace` part of your vscode. Not `user` part of your vscode.

```
{
  // config related to code formatting
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.detectIndentation": false,
  "editor.insertSpaces": false,
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": null
  },
  "javascript.validate.enable": false, //disable all built-in syntax checking
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },
  "eslint.alwaysShowStatus": true,
  // emmet
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  }
}
```

Next you have to add this line in your `package.json` file in your `scripts` object.

```
"lint": "yarn add prettier@latest --dev && yarn add @babel/eslint-parser@latest --dev && npx install-peerdeps@latest --dev eslint-config-airbnb@latest && yarn add eslint-config-prettier@latest eslint-plugin-prettier@latest eslint@latest eslint-config-airbnb@latest eslint-plugin-import@latest eslint-plugin-jsx-a11y@latest eslint-plugin-react@latest eslint-plugin-react-hooks@latest --dev"
```

Finally run the command in your terminal.

```
yarn lint
```

Make sure you have install yarn globally. To install yarn globally, type this command in your terminal

```
npm install -g yarn
```

## Authors

- [Webphics](https://webphics.com/)

## License

MIT License

Copyright (c) 2023 Webphics

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Feedback

If you have any feedback, please reach out to us at info@webphics.com
