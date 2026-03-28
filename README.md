# New York Public Library's Marp Template

Use [Marp](https://marp.app/) to create NYPL themed slide decks from markdown files.

* [Sample PDF output](https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/sample.pdf).

![usage](https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/assets/header.png)

> [!NOTE]
> This is an early version of the template and has not been audited by the communications team. We recommend using it for internal presentations only. Please reach out to the communications team if you intend to use this template for public-facing presentations.

## Usage

There are two ways to use this template: CLI and VS Code extension.

### CLI

```sh
$ git clone https://github.com/NYPL/nypl-marp-template.git
$ cd nypl-marp-template
```

With `npx` command, run:

```sh
$ npx @marp-team/marp-cli sample.md --theme-set ./themes/nypl-marp-template.scss --pdf
$ npx @marp-team/marp-cli sample.md --theme-set ./themes/nypl-marp-template.scss --pdf -w # watch mode for live preview
```

### VS Code

* Install extention: [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
* Go to settings and search for `markdown.marp.themes`
* Add the following url

```text 
https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/themes/nypl-marp-template.scss
```

* Open your markdown file in VS Code.  
* Use the VS Code command palette (`Ctrl+Shift+P` or `Cmd+Shift+P`) and search for "Marp: Export Slide Deck" to export your slides as PDF or PowerPoint.

## Contributing

PRs are widely welcome especially for improving themes.