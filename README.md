# Miking Language VSCode Extension

![GitHub package.json version](https://img.shields.io/github/package-json/v/miking-lang/miking-vscode)
![GitHub last commit](https://img.shields.io/github/last-commit/miking-lang/miking-vscode)

This repository contains the VSCode extension to support Miking Programming Language (MCore). Currently it only provides syntax highlighting but it could be extended to handle other development helpers such as snippet insertion, auto formatting and more. The syntax highlighting feature is currently limited to a declarative language support (using the `syntax/mcore.tmLanguage.json` grammar file) but could be enhanced with more [programmatic language features leveraging a language server](https://code.visualstudio.com/api/language-extensions/overview).

### Installation
Either build the the extension with
```
npm install
```
followed by
```
npm run package
```
This will produce a `vsix` file in the root directory. Alternatively you can download a pre-built `vsix` file from the [releases](https://github.com/miking-lang/miking-vscode/releases) page.

To install the extension in vscode run
```
code --install-extension <path/to/vsix>
```

### :rocket: Release a new version
A new extension version is released just by creating a Git tag and pushing it to the remote (GitHub). Then a GitHub Actions pipeline is triggered which builds and publishes the extension. A new GitHub release is also automatically created but is the duty of the publisher to add eventual changelog entries both to the CHANGELOG file in the repo and to the GitHub release.

The pipeline makes a new extension version available in two ways:
1. by packaging the extension in `vsix` file and uploading it to the release assets on GitHub
2. **TODO** by publishing the extension on VSCode Marketplace
