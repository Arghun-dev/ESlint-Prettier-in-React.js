# ESlint-Prettier-in-React.js

### 1.Install Eslint Globally

`$. npm i -g eslint`



### 2. Open your create-react-app react project or create one by typing

`$. npx create-react-app name-of-project`



### 3. Initiate Eslint in your project:

`$. eslint --init`



### 4. Then answer the question

### 5. Confirm installation of eslint-plugin-react

### 6. Leave this in your ESlint config:

```js
"env": {
      "browser": true,
      "es6": true
},
"extends": ["eslint:recommended"],
"plugins": ["react"],
"parserOptions": {
      "ecmaVersion": 2018
},
"rules": {}
```


### 7. Install eslint-config-react-app peer dependencies:

`$. npm install-peerdeps --dev eslint-config-react-app`



### 8. Install prettier dependencies:

`$. npm i -D eslint-config-prettier eslint-plugin-prettier prettier`



### 9. Configure Prettier through ESlint example:

```js
{
    "env": {
        "browser": true,
        "es6": true
    },
    "extends": ["react-app", "prettier"],
    "plugins": ["react", "prettier"],
    "parserOptions": {
        "ecmaVersion": 2018
    },
    "rules": {
        "prettier/prettier": [
            "error",
            {
                "printWidth": 80,
                "trailingComma": "es5",
                "semi": false,
                "jsxSingleQuote": true,
                "singleQuote": true,
                "useTabs": true
            }
        ]
    }
}
```


### 10. Change your VScode settings

`$. "eslint.autoFixOnSave": true`


### 11. Check for conflicting rules with the following script in package.json:

```js
{
    "scripts": {
        "eslint-check": "eslint --print-config path/to/main.js | eslint-config-prettier-check"
    }
}
```

**Happy Coding!**
