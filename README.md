# nypl-marp-template

New York Public Library's Marp Template

![usage](https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/assets/vscode.png)

## Usage

### CLI

Install Marp CLI and run:

```sh
$ npx @marp-team/marp-cli@latest sample.md --theme-set ./themes/nypl-marp-template.scss -o output.pdf
```

Watch mode for live preview:

```sh
$ npx @marp-team/marp-cli@latest sample.md --theme-set ./themes/nypl-marp-template.scss -o output.pdf -w
```

### VS Code

* Install extention: `Marp for VS Code`
* Go to settings and search for `markdown.marp.themes`
* Add the following urls:
  * http://example.com/nypl-marp-template/marp-theme.css
