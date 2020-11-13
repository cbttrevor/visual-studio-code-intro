## Learning Objectives

You're probably used to firing up Visual Studio Code from the Windows Start Menu, or maybe Spotlight if you're on Mac.
However, you can also launch VSCode using the command line.
You can invoke VSCode by simply calling `code` at a terminal.

**NOTE**: If you get an error when running `code`, you might need to reinstall the product.

### Manage VSCode Extensions

You can manage extensions for Visual Studio Code via the command line.
This is especially useful if you need to repeatedly build your development environment from scratch, or ensure multiple dev environments are in sync.
You can use a configuration management tool, such as Ansible, to help streamline the installation of extensions for VSCode.

#### Install a VSCode Extension

To install an extension in VSCode, you'll need to know the unique identifier of the extension. 
You can find this out by visiting the extension's page on the VSCode Marketplace.
For example, here is the page for the [VSCode Docker extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker).
The unique ID of the extension is `ms-azuretools.vscode-docker`.
Now let's use the `--install-extension` argument to install it!

```
code --install-extension ms-azuretools.vscode-docker
```

#### List Installed Extensions

To get a list of extensions that are currently installed, you can use the `--list-extensions` argument.

```
code --list-extensions
```

Using PowerShell, you can filter down the list of extensions to ones that match a given expression.
For example, if you were looking for Docker-related extensions, you could use the following command.

```
(code --list-extensions) -match 'docker'
```

### VSCode Command Line Help

If you forget the name of an argument for the `code` CLI, you can always use `--help` to print out the built-in documentation.

```
code --help
```