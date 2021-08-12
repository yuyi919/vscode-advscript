# How does the extension work?

The extension must be compiled from TypeScript to JavaScript and installed in VS Code.

Here is a high-level setup of how this particular the extension works:


## Command-prompt

The **command** will be added to the command-prompt section as it is defined under `"contributes"` in [package.json][]. You could add other triggers like buttons or drop-list menu items.


## Activate

To start the extension, the [extension.ts][] script needs to have an `activate` and `deactivate` function. For this simple project, this is only the script in `src`, besides the `test` scripts.

Note that the `activate` function is only called **once** to setup the extension. This is usually on IDE startup, but some extensions like the Python one only activate when you open a `.py` file.


## Register commands

One or more **commands** must be specified in [extension.ts][].

For example:

```javascript
vscode.commands.registerCommand('quickstart.helloWorld', () => {
    // ...
});
```

Commands will actually run whenever they are triggered by an event such as with a button click or when invoked using a menu or prompt.


## Actions

The Hello World **notification event** will be pushed using this line in [extension.ts][].

```javascript
vscode.window.showInformationMessage('Hello World from Quickstart!');
```

[extension.ts]: /src/extension.ts
[package.json]: /package.json
