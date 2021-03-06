# Flex Standard Layout using CSS Flexbox in Angular

This is a bare bone Standard 3 row(header, main, footer) layout using CSS Flexbox for Angular website.

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.1

There are 2 ways you can launch the application :

1. Application is hosted on `Github Pages`, you can launch the application on your browser directly, by [clicking here](https://kumaran-is.github.io/flex-standard-layout).

2. Launch the application on [StackBlitz](https://stackblitz.com/), by [clicking here](https://stackblitz.com/github/kumaran-is/flex-standard-layout). [StackBlitz](https://stackblitz.com/) is a online code editor built on top of vscode editor, where you can edit and see your changes on the fly.

**Table of contents:**

1. [Prerequisites and Installation](#prerequisites-and-installation)
1. [Quick Start](#quick-start)
1. [Build Tasks and Commands](#build-tasks-and-commands)
1. [Profiling the Build](#profiling-the-build)
1. [Publish Angular Application to Github Pages](#publish-angular-application-to-github-pages)
1. [GitHub Working Agreement](#github-working-agreement)
1. [Changelog](#changelog)
1. [Issue Tracker](#issue-tracker)

## Prerequisites and Installation

Library | Version | Notes
:-------|:--------:|-------
[Node](https://nodejs.org/) | 10.15.0 | Recommended NodeJS version
[NPM](https://nodejs.org/) |6.4.1 | Recommended NPM version
[Angular](https://angular.io/) | ~7.2.x | JavaScript-based open-source front-end SPA framework
[Angular CLI](https://github.com/angular/angular-cli) | ~7.3.0 | Set of development tools for Angular

## Quick Start

To launch the application on your computer, you can try below steps:

1. Clone repository and checkout the `master` branch

    ```bash
    git clone https://github.com/kumaran-is/flex-standard-layout.git
    cd flex-standard-layout
    git checkout master
    ```

1. Install NPM dependencies

    ```bash
    npm install
    ```

1. Run linting

    ```bash
    npm run lint
    ```

1. Start application in development mode

    ```bash
    ng serve -o
    ```

1. Application opens in browser [http://localhost:4200](http://localhost:4200)

## Build Tasks and Commands

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular Official Site for Angular CLI Overview and Commands](https://angular.io/cli).

## Profiling the Build

The more the application grows, the slower the build gets. Angular CLI version 7.0.0 introduced a --profile flag that outputs the build events and lets you profile them in chrome://tracing. You can use this feature as follows:

1. Build your project with --profile flag on (ng build --prod --profile)
2. Angular CLI will produce a file called chrome-profiler-events.json
3. Open [chrome://tracing](chrome://tracing/) and click on “Load” in the top left corner
4. Select chrome-profiler-events.json
5. For more detail refer the [link](https://blog.mgechev.com/2019/02/06/5-angular-cli-features/)

## Publish Angular Application to Github Pages

`Github Pages` is a Github feature that allows you to deploy any static website or web application or Angular application from your `gh-pages` branch to `Github Pages` for free

Using [angular-cli-ghpages](https://www.npmjs.com/package/angular-cli-ghpages) library, you can easily publish your angular application to `Github Pages`.

1. Install [angular-cli-ghpages](https://www.npmjs.com/package/angular-cli-ghpages) as a devDependency to your project

    ```bash
    npm install angular-cli-ghpages --save-dev
    ```

1. Add below npm script to your `package.json`

    ```bash
    "scripts": {
      ....
      .....
      "prod-build": "ng build --prod --base-href=./",
      "git-publish": "npm run prod-build && npx angular-cli-ghpages --dir=dist/flex-standard-layout --branch=gh-pages"
    }
    ```

1. Publish your application from `gh-pages` branch to `Github Pages`. Branch `gh-pages` is automatically created for you. Command below,
first runs production build, automatically commits and pushes the changes from 'dist' folder to `gh-pages` branch and deploys it to `Github Pages`.
Branch `gh-pages` act as a staging folder for deployment.

    ```bash
    npm run git-publish
    ```

1. Launch your application on browser by navigating to `https://username.github.io/repo-name/`. Example to launch this application click this link <https://kumaran-is.github.io/flex-standard-layout>

1. For more detail and options, refer the official [angular-cli-ghpages](https://www.npmjs.com/package/angular-cli-ghpages) github.

## GitHub Working Agreement

We will be working off the master branch. When working on a new feature or fixing a bug,
create a new branch out of the master branch and follow the below naming convention for the branch name.
Remember that GitHub and MacOS are case-sensitive. Our standard will be for all branch names and file
names to be all lower-case.

 - **For features**: feature/{feature-name}
    - Example:
                
            git checkout -b feature/auth_flow  # using feature name
 - **For bugs**: fix/{bug-name}
    
    - Example:
             git checkout -b fix/login_fails  # using  bug name


Before submitting a Pull Request for the  repository make sure to check the following:

  - There should be zero jshint and jscs errors.
  - Make sure the application runs without any errors.
  - Code coverage does not drop under 80%
  - All possible test cases are added, both happy path and failure path like exceptional or error conditions.  
  - Pull Request would be reviewed by me.
  - As a reviewers i`ll verify:
    - `npm run lint` should pass
    - Verify PR code changes works as expected by running it on local machine
    - No errors in the browser console
    - Review the code changes to makesure it is written as per Angular coding standard recommended in [angular.io](https://angular.io/) for syntax, conventions, and structuring Angular application.
    - Review if any changes needed to Readme prescription or any project documents
    - Review the changelog and application version
    - Delete the branch after merging back with the master branch.

## Changelog

* [Changelog](./CHANGELOG.md).

## Issue Tracker

* [Issue tracker](https://github.com/kumaran-is/flex-standard-layout/issues?state=open)
