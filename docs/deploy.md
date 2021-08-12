# Deploy


## Export

You can _export_ your extension as an archive file.

Then it can be _installed_ globally for yourself and shared with others so they can install it too. That is more permanent than running in debug mode as covered in the [Development](development.md#start-the-extension) doc.


## Publish

You can also _publish_ the extension to the VS Code Marketplace so it can be found easily.

See my guides for how to export, install and publish a VSIX extension file.

- [Export and publish extension](https://michaelcurrin.github.io/dev-cheatsheets/cheatsheets/vscode-extensions/extension/) in my Dev Resources. There are links to VS Code's instructions which are friendly for beginners publishing for the first time.
- [VS Code extensions](https://michaelcurrin.github.io/dev-cheatsheets/cheatsheets/other/vscode-extensions/) in my Dev Cheatsheets


## CI

If you want to run automated checks in the cloud like formatting, linting, and unit tests, I recommend using [GitHub Actions][].

See my [Auto Commit Message][] repo, which has that set up in `.github/workflows`.

[GitHub Actions]: https://michaelcurrin.github.io/dev-resources/resources/ci-cd/github-actions/
[Auto Commit Message]: https://github.com/MichaelCurrin/auto-commit-msg
