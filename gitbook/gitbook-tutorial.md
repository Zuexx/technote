# Setup GitBook CLI

## Prerequisite

[nvm-link]: https://github.com/coreybutler/nvm-windows

- [Manage multiple installations of node.js on a Windows computer][nvm-link]
- Use nvm to specify the node.js version to use **v13.14.10**

  - _due to the official gitbook-cli did not maintain anymore that we need to specify the particular version of node.js to make all the setting execution as expected._

  - List the installed version of node.js
    ```bash
    nvm list
    ```
  - Install the particular version of node.js
    ```bash
    nvm install 13.14.0
    ```
  - Specified the particular version of node.js
    ```bash
    nvm use 13.14.0
    ```

## Install GitBook CLI via NPM or YARN

```bash
npm install -g gitbook-cli
```

Make sure your environment already has YARN installed.
If not, please install yarn properly first.

```bash
npm install -g yarn
```

Then use the following command to install gitbook

```bash
yarn global add gitbook-cli
```

## GitBook Folder Structure

&nbsp;&nbsp;&nbsp;&nbsp;_Figure for GitBook folder structure_

## Reference Information

[ref-01-link]: https://www.onejar99.com/how-to-build-and-publish-your-own-gitbook-free-unlimitedly-and-automatically-using-github-pages-and-github-actions/

- [How to build and publish your own GitBook free, unlimitedly, and automatically: using GitHub Pages and GitHub Actions][ref-01-link]
