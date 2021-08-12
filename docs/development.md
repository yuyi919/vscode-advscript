# Development
> Tips for developers using this repo

Make sure you follow the [Installation](installation.md) guide first.


## Run lint checks

```sh
$ npm run lint:check
```

## Fix linting issues

```sh
$ npm run lint:fix
```


## Run tests

```sh
$ npm test
```

That will also run the TypeScript compile step.

Note that you must **exit** all instances of VS Code to run the tests, or you'll get this error:

```
[main 2021-01-13T15:54:07.713Z] Running extension tests from the command line is currently
only supported if no other instance of Code is running.
```

Note - with VS Code was closed, I found this test step runs and gets stuck with the instance open. I don't know if that was always the case.

You can also run tests with VS Code **open** using another approach below.

### Run tests in Debug mode

Open _Debug_ tab in VS Code.

Click run for _Extension Tests_.

That will open up another VS Code window with the extension added and it will run tests.

It is useful to have VS Code run lighter without other extensions. While not part of the quickstart, see the `--disable-extensions` flag added in [launch.json](/.vscode/launch.json) arguments.


## Commands

See available script commands in [package.json](/package.json) by running this:

```sh
$ npm run
```


## Start the extension
> Run temporarily in debug mode

Open the _Debug_ tab in VS Code then click _Run Extension_.

That will run the extension in a sandboxed environment in a new window - the extension is not installed in other windows and you won't be able to use the extension after you close the window.

That will run the watch command which compiles the app and then watches the directory for changes.

If you want to install the extension globally and so that is persists, see the [Deploy](deploy.md) doc.
