# Introduction

This is a boilerplate for React component npm package development.
The actuall component code is under `/package`, and the test website is under `/example`.

# Before start development

- Update package name, description, and repo url in `/package/package.json`.
- Delete `.git` folder to clean the repo remote link and commit history
- Add remote url be running the command below
  ```
  git remote add origin [your-repo-url]
  ```

# Local development

1. Install npm packages if this is the first time you're trying to run. You will need to run the command below under both `/example` and `/package` directories.

   ```
   npm install
   ```

2. Run the command below under `/package` folder to add your local package to your local npm package pool.

   ```
   npm link
   ```

3. Run the command below to be able to use the local version of your package in the `example` website. **Remember to update the package name in `/package/package.json` to your package name.**

   ```
   npm link [your-package-name]
   ```

4. Run the command below under both `/package` and `/example` to start development. When you make a change in the package source code, your example website will hot reload the changes.

   ```
   npm start
   ```

# Configurations

- eslint - `.eslintrc.json` (the project uses airbnb react rule set)
- babel - `.babelrc`
- webpack - `webpack.config.js`
- editor coding style - `.editorconfig` (if you use VSCode, you'll need to install `editorconfig` extension to be able to use it)

# Scripts

## package

- `npm test` - run unit tests of your component
- `npm start` - build dev version (non-minified code) and watching changes
- `npm run build` - build prod version (minified code)

## example

- `npm start` - start website
