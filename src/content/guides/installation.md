---
title: Installation
sort: 1
contributors:
  - pksjce
  - bebraw
  - simon04
---

This guide goes through the various methods used to install webpack.


## Pre-requisites

Before we begin, make sure you have a fresh version of [Node.js](https://nodejs.org/en/) installed. The current Long Term Support (LTS) release is an ideal starting point. You may run into a variety of issues with the older versions as they may be missing functionality webpack and/or its related packages require.


## Local Installation

The latest webpack release is:

[![GitHub release](https://img.shields.io/npm/v/webpack.svg?label=webpack&style=flat-square&maxAge=3600)](https://github.com/webpack/webpack/releases)

To install the latest release or a specific version, run one of the following commands:

``` bash
npm install --save-dev webpack
npm install --save-dev webpack@<version>
```

Installing locally is what we recommend for most projects. This makes it easier to upgrade projects individually when breaking changes are introduced. Typically webpack is run via one or more [npm scripts](https://docs.npmjs.com/misc/scripts) which will look for a webpack installation in your local `node_modules` directory:

```json
"scripts": {
	"start": "webpack --config webpack.config.js"
}
```

T> To run the local installation of webpack you can access its bin version as `node_modules/.bin/webpack`.


## Global Installation

The following NPM installation will make `webpack` available globally:

``` bash
npm install --global webpack
```

W> Note that this is __not a recommended practice__. Installing globally locks you down to a specific version of webpack and could fail in projects that use a different version.


## Bleeding Edge

If you are enthusiastic about using the latest that webpack has to offer, you can install beta versions or even directly from the webpack repository using the following commands:

``` bash
npm install webpack@beta
npm install webpack/webpack#<tagname/branchname>
```

W> Take caution when installing these bleeding edge releases! They may still contain bugs and therefore should not be used in production.
