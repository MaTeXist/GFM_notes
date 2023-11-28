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

### 表格（table）

```Markdown
|默认左对齐|左对齐|居中对齐|右对齐|
|-|:-|:-:|-:|
|foo|bar|baz|qux|
```

单元格内容和`|`之间的空格会被忽略。

#### 锚点

```Markdown
[锚点](#文本格式)
```

[锚点](#文本格式)



