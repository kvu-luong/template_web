### Documentation
1. [Video Tutorial](https://www.youtube.com/watch?v=Iu5aZDqZt8E)
2. Running app
   ```
   yarn dev
   ```
### Check list:
- [x] Create project
- [x] Engine lock
- [x] Eslint
- [x] Prettier
- [x] Husky: pre-commit, commit message
- [ ] Vscode configuration
- [ ] Storybook
- [ ] Webpack with multiple environment
- [ ] Hexagon architecture


1. Create a NextJs application
   ```bash
    npx create-next-app@latest
   ```
2. Setting node engine with **.nvmrc** file
3. Setting package type with **.npmrc** file and **package.json** in engine section.
   ```bash
     "engines": {
        "node": ">=18.15.0",
        "yarn": ">=1.22.19",
        "npm": "please-use-yarn"
     },
   ```
4. Adding lint package
    ```bash 
        #running lint to check error warning with eslint
        yarn lint
    ```
    [Eslint rules](https://eslint.org/docs/latest/rules/)
5. Adding Prettier
    ```bash 
        yarn add -D prettier
    ```
    - Then add vscode extension: <i>Prettier - Code format</i>.
    - Create two more files: **.prettierignore** and **.prettierrc**
    - [Prettier playground](https://prettier.io/playground/)
    - [Documentation](https://prettier.io/docs/en/install.html)
    - [Checking Node Version Compatible](https://gist.github.com/chranderson/b0a02781c232f170db634b40c97ff455)
        ```bash 
            # check version
            node -v || node --version

            # list locally installed versions of node
            nvm ls
            # list remove available versions of node
            nvm ls-remote

            # install specific version of node
            nvm install 18.16.1

            # set default version of node
            nvm alias default 18.16.1

            # switch version of node
            nvm use 20.5.1
        ```
6. Adding Husky
   - Setup husky: pre-commit and pre-commit 
        ```bash
        yarn add -D husky

        #Install husky 
        npx husky install 

        #Adding pre commit 
        npx husky add .husky/pre-commit "yarn lint"

        #Adding push commit
        npx husky add .husky/pre-push "yarn build"

        #Adding husky script
        npm pkg set scripts.prepare="husky install"
        ```

    - Start setup commit lint
  
        [Reference documentation](https://github.com/conventional-changelog/commitlint)

        ```bash 
            #Install commit lint
            yarn add -D @commitlint/{config-conventional,cli}

            #Create file commit lint
            echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js

            #Adding script
            npx husky add .husky/commit-msg  'npx --no -- commitlint --edit ${1}'
        ```
7. Vscode setup
   Create a folder .vscode and update the content of configuration in **setting.json** file.

