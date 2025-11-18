# Use Volta for Node.js Version Management

## Context

As JS developers, we often need to manage multiple versions of Node.js across different projects. Installing and switching between these versions manually can be cumbersome and error-prone. If an engineer forgets to use the correct Node.js version for a project, it can lead to unexpected bugs and inconsistencies that are hard to debug. 

### Project Overview

N/A - this is an example, not a real project.

### Problem Statement

Manually managing the correct node/npm version for a project is cumbersome and error-prone, leading to a lot of "works on my machine" issues.

## Decision

Use Volta (https://volta.sh/) to manage Node.js versions for this project. Volta allows us to specify the Node.js version in a `package.json` file, and it automatically ensures that the correct version is used whenever we run Node.js commands in the project directory.

### Options

#### [Volta](https://volta.sh/)

Volta is a JavaScript tool manager written in Rust that leverages a simple declarative config in package.json. When `node` or `npm` commands are run in a package that has a Volta config, it transparently fetches and switches to the correct versions.

Pros:
* Easy to set up and use.
* No need to manually switch versions (operates automatically).
* Cross platform support (macOS, Linux, Windows).
* Supports pinning versions of Node.js, npm, yarn, and global binaries.
* Fast performance due to being written in Rust.
* Integrates with Github Actions via the `node-version-file` argument.

Cons:
* Not as ubiquitous as nvm in some environments.

#### [nvm](https://github.com/nvm-sh/nvm)

nvm (Node Version Manager) is a popular bash script that allows users to install and switch between multiple versions of Node.js. It relies on an `.nvmrc` file to specify the desired Node.js version for a project. Developers must remember to run `nvm use` to switch to the correct version when working on different projects.

Pros:
* Widely used and well-known in the JavaScript community.
* Simple to set up and use.
* No runtime performance overhead at all due to architecture.

Cons:
* No Windows support, although there is a separate project called nvm-windows.
* Requires manual switching between versions, which can lead to errors if forgotten.

## Consequences

We don't anticipate any negative consequences from this decision. Volta can be used in the same repository as other version managers if needed, but we expect that using Volta alone will suffice for our needs. All team members should install Volta to ensure consistency.
