---
marp: true
theme: nypl
paginate: true
---

<!-- _class: title -->

# NYPL Marp Template

Markdown-based presentation template for The New York Public Library

![bg right 40%](https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/assets/logo-with-text.png)

---

# What is Marp?

* [Marp](https://marp.app/) is a markdown presentation ecosystem. It provides a CLI tool to convert markdown files into PDF, PowerPoint, and HTML slide decks.

* Syntax is based on GitHub Flavored Markdown, so you can write slides in a familiar way.
* Inserting `---` creates a new slide.

---

# How to write slides

Add a YAML front matter to the top of your markdown file...

```yaml
---
marp: true
theme: nypl
---
```

...and split pages by horizontal ruler (`---`). It's very simple!

```markdown
# Slide 1

foobar

---

# Slide 2

foobar
```

---

# How to convert to PDF or PowerPoint (CLI)

Run following commands in your terminal:

```sh
# PDF output
$ npx @marp-team/marp-cli@latest sample.md --theme-set ./css

# Watch mode for live preview
$ npx @marp-team/marp-cli@latest sample.md --theme-set ./css -w
```

---

# How to preview in VS Code

## Setup

* Install extention: [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
* Go to settings and search for `markdown.marp.themes`
* Add the following url:

```text
https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/themes/nypl-marp-template.scss
```

## Usage

* Open your markdown file in VS Code.  
* Press `Ctrl+Shift+V` (or `Cmd+Shift+V` on Mac) to open the Marp preview pane.
* Use the VS Code command palette (`Ctrl+Shift+P` or `Cmd+Shift+P`) and search for "Marp: Export Slide Deck" to export your slides as PDF or PowerPoint.

---

# Workflow example

Pane feature in VS Code is handy to edit markdown and preview slides side by side.

![w:900](https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/assets/vscode.png)

---

# Code block (JS/TS, Python)

Supports syntax highlighting.

```typescript
function fibonacci(n) {
  let a = 0, b = 1;
  for (let i = 0; i < n; i++) {
    [a, b] = [b, a + b];
  }
  return a;
}

console.log(fibonacci(10));  // Output: 55
```

```python {numberLines: true}
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a

print(fibonacci(10))  # Output: 55
```


---

# Code block (Ruby, Diff)


```ruby
def fibonacci(n)
  a, b = 0, 1
  n.times do
    a, b = b, a + b
  end
  a
end

puts fibonacci(10) # Output: 55
```

```diff
- old line
+ new line
```

---

# Tables

Supports table markdown syntax. 

**Example:**

```markdown
| Header | Header | Header | Center | Right |
| ------ | ------ | ------ | :----: | ----: |
| Cell   | Cell   | Cell   |  Cell  |  100% |
| Cell   | Cell   | Cell   |  Cell  |   50% |
| Cell   | Cell   | Cell   |  Cell  |   30% |
```

**Output:**

| Header | Header | Header | Center | Right |
| ------ | ------ | ------ | :----: | ----: |
| Cell   | Cell   | Cell   |  Cell  |  100% |
| Cell   | Cell   | Cell   |  Cell  |   50% |
| Cell   | Cell   | Cell   |  Cell  |   30% |

---

# Headers

# H1

H1 is usually reserved for slide title. We recommend using `H2` - `H4` for content.

## H2

NYPL’s Mission Statement

### H3

The mission of The New York Public Library is to inspire lifelong learning, advance knowledge, and strengthen our communities.

#### H4

To deliver on this promise, we rely on three great resources—our staff, our collections, and our physical and digital spaces—to provide opportunities for learning and growth to all New Yorkers.

---

# Text formatting

**Bold** text is supported, as well as *italic* and ***bold italic***. You can also create lists:

- Unordered list item 1
- Unordered list item 2
  - Unordered list item 3
  - Unordered list item 4

1. Ordered list item 1
2. Ordered list item 2
3. Ordered list item 3

---

# Links and images

You can insert links and images using markdown syntax. With size modifiers (e.g. `w:300 left`), you can adjust the size of images to fit your slides.

## Links

- [NYPL website](https://www.nypl.org/)

## Images

![w:250 left](https://raw.githubusercontent.com/NYPL/nypl-marp-template/refs/heads/main/assets/logo-with-text.png)

---

# Math formulas

We could also use $\LaTeX$ syntax. Wrap formula in `$$` to render it as a block, or in `$` to render it inline.

$$
I_{xx}=\int\int_Ry^2f(x,y)\cdot{}dydx
$$

---

<!-- _class: inverted -->

# Thank you!