
1 - npm install 

2 - npm i -D prettier eslint 

"devDependencies": {
    "eslint": "^7.19.0",
    "prettier": "^2.2.1"
  },


3 - installer les 2 extention prettier et eslint sur VScode


4 - >npx eslint --init

√ How would you like to use ESLint? · style

√ What type of modules does your project use? · commonjs

√ Which framework does your project use? · none

√ Does your project use TypeScript? · No / Yes

√ Where does your code run? · browser

√ How would you like to define a style for your project? · guide

√ Which style guide do you want to follow? · airbnb

√ What format do you want your config file to be in? · JSON

Checking peerDependencies of eslint-config-airbnb-base@latest


5 - fair passer prettier avant eslint 


  npm i -D eslint-config-prettier eslint-plugin-prettier

6 - configurer eslintrc.json

 {

  "env": {

    "browser": true,

    "commonjs": true,

    "es2021": true

  },

  "extends": ["airbnb-base", "prettier"],

  "plugins": ["prettier"],

  "parserOptions": {

    "ecmaVersion": 12

  },

  "rules": {

    "prettier/prettier": [

      "error",

      {

        "endOfLine": "auto"

      }

    ],

    "import/no-extraneous-dependencies": "off",

    "import/prefer-default-export": "off",

    "no-confusing-arrow": "off",

    "linebreak-style": "off",

    "arrow-parens": ["error", "as-needed"],

    "comma-dangle": [

      "error",

      {

        "arrays": "always-multiline",

        "objects": "always-multiline",

        "imports": "always-multiline",

        "exports": "always-multiline",

        "functions": "ignore"

      }

    ],

    "no-plusplus": "off"

  }
  

}

7 - go to settings VScode -> workspace

   Tabe size :2 

   cocher le Formate on save 

     -W generate .vscode/settings.json 

      config : 

       {

          "editor.formatOnSave": true,

          "editor.tabSize": 2,

          "[javascript]": {

            "editor.formatOnSave": false

          },

          "editor.codeActionsOnSave": {

            "source.fixAll": true

          }
          
        }



// ------------------------------ OR Clone the ripo :p !!! 

utilities 
fix the buges : eslint . --fix


Links :
airbnb rules : https://github.com/airbnb/javascript