# How to contribute

I love pull requests. And following this simple guidelines will make your pull request easier to merge.

## Submitting pull requests

1.  Create a new branch, please don’t work in master directly.
2.  Add failing tests (if there’re any tests in project) for the change you want to make. Run tests (see below) to see the tests fail.
3.  Hack on.
4.  Run tests to see if the tests pass. Repeat steps 2–4 until done.
5.  Update the documentation to reflect any changes.
6.  Push to your fork and submit a pull request.

## JavaScript code style

[See here](https://github.com/tamiadev/eslint-config-tamia#code-style-at-a-glance).

## VSCode Devcontainer on Windows

Development on this project currently does not work on Windows, but there is a workaround: [Developing inside a Container.](https://code.visualstudio.com/docs/remote/containers#:~:text=A%20devcontainer.json%20file%20in%20your%20project%20tells%20VS,or%20runtimes%20needed%20for%20working%20with%20a%20codebase.) The **devcontainer.json** file in the repo tells VS Code how to access (or create) a development container. You will need:

- [Visual Studio Code](https://code.visualstudio.com/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) on Windows 10+

To get good performance, used the Start VS Code and run **Dev Containers: Clone Repository in Container Volume...** from the Command Palette (F1), then enter the URL of your fork of the project. This will create a Linux VM/container and clone the repo into it. This is almost transparant once set up, except you get the bash shell by default, instead of PowerShell when you open terminal windows. It even takes care of installing dependencies and running Lerna Bootstrap.

## Other notes

- If you have commit access to repository and want to make big change or not sure about something, make a new branch and open pull request.
- Don’t commit generated files: compiled from Stylus CSS, minified JavaScript, etc.
- Don’t change version number and change log.
- Install [EditorConfig](http://editorconfig.org/) plugin for your code editor.
- Feel free to [ask me](http://sapegin.me) anything you need.

## Building and running tests

_Run these commands in the root folder of the repository._

Install dependencies and bootstrap [Lerna](https://github.com/lerna/lerna):

```bash
npm run bootstrap
```

Run tests for all packages:

```bash
npm test
```

Or run a watch mode:

```bash
npm run test:watch
```
