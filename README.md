## GitHub Flavored Markdown

### 文本格式

#### 行内代码（inline code）

In issues, pull requests, and discussions, you can call out colors within a sentence by using backticks. A supported color model within backticks will display a visualization of the color.

```Markdown
The background color is `#ffffff` for light mode and `#000000` for dark mode.
```

Here are the currently supported color models.

|Color|Syntax|Example|
|:-:|:-:|:-:|
|HEX|`#RRGGBB`|`#0969DA`|
|RGB|`rgb(R,G,B)`|`rgb(9, 105, 218)`|
|HSL|`hsl(H,S,L)`|`hsl(212, 92%, 45%)`|

#### 删除线（strikethrough）

```Markdown
~~我被删除了~~
```

### 图像（image）

GitHub supports embedding images into your issues, pull requests, discussions, comments and .md files. You can display an image from your repository, add a link to an online image, or upload an image.

### 表格（table）

```Markdown
|默认左对齐|左对齐|居中对齐|右对齐|
|-|:-|:-:|-:|
|foo|bar|baz|qux|
```

单元格内容和`|`之间的空格会被忽略。

### 链接（link）

#### 节链接（section link）

```Markdown
[锚点](#某标题)
```

#### 相对链接（relative link）

You can define relative links and image paths in your rendered files to help readers navigate to other files in your repository.

A relative link is a link that is relative to the current file. For example, if you have a README file in root of your repository, and you have another file in docs/CONTRIBUTING.md, the relative link to CONTRIBUTING.md in your README might look like this:

```Markdown
[Contribution guidelines for this project](docs/CONTRIBUTING.md)
```

GitHub will automatically transform your relative link or image path based on whatever branch you're currently on, so that the link or path always works. The path of the link will be relative to the current file. Links starting with / will be relative to the repository root. You can use all relative link operands, such as `./` and `../`. `./`表示当前目录，`../`表示上级目录。

Relative links are easier for users who clone your repository. Absolute links may not work in clones of your repository - we recommend using relative links to refer to other files within your repository.
