1. `yarn create react-app my-app`

2. `yarn start`

3. Apagar arquivos desnecessários

4. Em package.json, apagar a parte do ESLINT

5. instalar extensão "editorconfig" no vscode

  5.1. clicar com o botão direito na área sem arquivos no explorer do vscode

  5.2. clicar em Generate .editorconfig

  5.3. setar *trim_trailing_whitespace* e *insert_final_newline* para true

  5.4. indent_size = 2

  5.5. end_of_line = lf

6. no terminal, intalar o eslint: `yarn add eslint -D`

7. iniciar configurações do eslint: `yarn eslint --init`

✔ How would you like to use ESLint? · style

✔ What type of modules does your project use? · esm

✔ Which framework does your project use? · react

✔ Does your project use TypeScript? · No / Yes

✔ Where does your code run? · browser✔ How would you like to define a style for your project? · guide

✔ Which style guide do you want to follow? · airbnb

✔ What format do you want your config file to be in? · JavaScript

✔ Would you like to install them now with npm? · No / **Yes**

8. Deletar:   package-lock.json

9. Atualizar os arquivos do yarn.lock. No terminal usar somente: `yarn`

10. Prettier: `yarn add prettier eslint-config-prettier eslint-plugin-prettier babel-eslint -D`

11. Em **.eslintrc.js**:

  11.1. Em extends add: 'prettier' e 'prettier/react

  11.2. Antes de parserOptions add: parser: 'babel-eslint',

  11.3. Em plugins, add: `'prettier'`

  11.4 Em rules:

    `rules: {
      'prettier/prettier': 'error',
      'react/jsx-filename-extension': [
        'warn',
        { extensions: ['.jsx', '.js'] }
      ],
      'import/prefer-default-export': 'off'
    },`

12. clicar com o botão direito na área sem arquivos no explorer do vscode e criar um arquivo **.prettierrc**

  12.1. colocar:

    `{
      "singleQuote": true,
      "trailingComma": "es5"
    }`
