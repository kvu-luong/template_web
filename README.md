### Documentation
1. [Video Tutorial](https://www.youtube.com/watch?v=Iu5aZDqZt8E)
2. Running app
   ```
   yarn dev
   ```
### Check list:
- [x] Create project
- [x] Engine lock/ Vscode
- [x] Eslint
- [x] Prettier
- [ ] Husky: pre-commit, commit lint
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
        #running lint
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
