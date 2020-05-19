
# What is this?

This template creates a private repository to store your private packages on your own machine using [Verdaccio](https://verdaccio.org/).

# How to use this?

Steps:
1. Pull this repo and install dependencies using `yarn` or `npm install`
2. Run the Verdaccio using `yarn verdaccio`, this will let you run verdaccio in http://localhost:4873
3. Add a user `npm adduser http://localhost:4873`.
    - create your username and password (for now)
    - By default, if you publish a package, verdaccio stores it in your local machine.
4. Create .npmrc and add this line to make verdaccio your default package repository. (Don't worry, if you install a package that is not in verdaccio, it will fallback to npm package registry)
    ```
    registry=http://localhost:4873
    ```
    

# TODOS:
- [x] Use AWS S3 to share packages (Update README)
- [ ] Use github OAUTH and whitelist only accounts in a certain organization
- [ ] Integrate lerna(monorepo) to let versioning of packages easier.
