## GitHub Flavored Markdown

### 字符

#### 表情（emoji）

使用一对`:`包裹表情代码，如：

|表情字符|表情代码|效果|
|:-:|:-:|:-:|
|😄|`:smile:`|:smile:|
|😆|`:laughing:`|:laughing:|
|👍|`:+1:`|:+1:|
|👎|`:-1:`|:-1:|
|👏|`:clap:`|:clap:|

For a full list of available emoji and codes, see the [Emoji-Cheat-Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).

#### 数学表达式（mathematical expressions）

使用 $\mathrm{\LaTeX}$ 的公式语法。

GitHub's math rendering capability uses MathJax; an open source, JavaScript-based display engine. MathJax supports a wide range of LaTeX macros, and several useful accessibility extensions.

##### 行内公式

There are two options for delimiting a math expression inline with your text. You can either surround the expression with dollar symbols (`$`), or start the expression with <code>$\`</code> and end it with <code>\`$</code>. The latter syntax is useful when the expression you are writing contains characters that overlap with markdown syntax.

```Markdown
This sentence uses `$` delimiters to show math inline: $a^2+b^2=c^2$.
```

This sentence uses `$` delimiters to show math inline: $a^2+b^2=c^2$.

Outside a math expression, but on the same line, use `span` tags around the explicit `$`.

```Markdown
To split <span>$</span>100 in half, we calculate $100/2$.
```

To split <span>$</span>100 in half, we calculate $100/2$.

##### 行间公式

To add a math expression as a block, start a new line and delimit the expression with two dollar symbols `$$`.

```Markdown
$$\left(\frac pq\right)\left(\frac qp\right)=(-1)^{\frac{(p-1)(q-1)}4}.$$
```

$$\left(\frac pq\right)\left(\frac qp\right)=(-1)^{\frac{(p-1)(q-1)}4}.$$

Alternatively, you can use the <code>\`\`\`math</code> code block syntax to display a math expression as a block.

````Markdown
The Cauchy-Schwarz Inequality:

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
```
````

The Cauchy-Schwarz Inequality:

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
```

### 文本格式

#### 行内代码（inline code）

In issues, pull requests, and discussions, you can call out colors within a sentence by using backticks. A supported color model within backticks will display a visualization of the color.

```Markdown
The background color is `#ffffff` for light mode and `#000000` for dark mode.
```

The background color is `#ffffff` for light mode and `#000000` for dark mode.

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

~~我被删除了~~

### 列表（list）

#### 嵌套列表（nested list）

Type space characters in front of your nested list item until the list marker character (`-` or `*`) lies directly below the first character of the text in the item above it.

In this example, you could add a nested list item under the list item 100. First list item by indenting the nested list item a minimum of five spaces, since there are five characters (100 .) before First list item.

```Markdown
100. First list item
     - First nested list item
```

100. First list item
     - First nested list item
    
#### 任务列表

```Markdown
- [ ] 未选中；
- [x] 已选中。
```

- [ ] 未选中；
- [x] 已选中。

### 图像（image）

GitHub supports embedding images into your issues, pull requests, discussions, comments and .md files. You can display an image from your repository, add a link to an online image, or upload an image.

#### Specifying the theme an image is shown to

You can specify the theme an image is displayed for in Markdown by using the HTML `<picture>` element in combination with the `prefers-color-scheme` media feature. We distinguish between light and dark color modes, so there are two options available. You can use these options to display images optimized for dark or light backgrounds. This is particularly helpful for transparent PNG images.

For example, the following code displays a sun image for light themes and a moon for dark themes:

```Markdown
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>
```

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

### 表格（table）

```Markdown
|默认左对齐|左对齐|居中对齐|右对齐|
|---|:---|:---:|---:|
|foo|bar|baz|qux|
```

|默认左对齐|左对齐|居中对齐|右对齐|
|---|:---|:---:|---:|
|foo|bar|baz|qux|

单元格内容和`|`之间的空格会被忽略。

The pipes `|` on either end of the table are optional.

There must be at least three hyphens in each column of the header row.

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

[Contribution guidelines for this project](docs/CONTRIBUTING.md)

GitHub will automatically transform your relative link or image path based on whatever branch you're currently on, so that the link or path always works. The path of the link will be relative to the current file. Links starting with / will be relative to the repository root. You can use all relative link operands, such as `./` and `../`. `./`表示当前目录，`../`表示上级目录。

Relative links are easier for users who clone your repository. Absolute links may not work in clones of your repository - we recommend using relative links to refer to other files within your repository.

#### 自动链接（autolink）

```Markdown
https://spec.commonmark.org/0.30/
```

https://github.com/Liyu-math/GFM_notes/tree/main

#### Referencing issues and pull requests

You can bring up a list of suggested issues and pull requests within the repository by typing `#`.

Within conversations on GitHub, references to issues and pull requests are automatically converted to shortened links. Autolinked references are not created in wikis or files in a repository.

#### Referencing external resources

If custom autolink references are configured for a repository, then references to external resources, like a JIRA issue or Zendesk ticket, convert into shortened links.

#### Uploading assets

You can upload assets like images by dragging and dropping, selecting from a file browser, or pasting. You can upload assets to issues, pull requests, comments, and .md files in your repository. When you attach a file, it is uploaded immediately to GitHub and the text field is updated to show the anonymized URL for the file.

```Markdown
[新建文本文档.txt](https://github.com/Liyu-math/GFM_notes/files/13486268/default.txt)
```

[新建文本文档.txt](https://github.com/Liyu-math/GFM_notes/files/13486268/default.txt)

### Commit SHAs

References to a commit's SHA hash are automatically converted into shortened links to the commit on GitHub.

#### A permanent link to a code snippet

### 引用块（blockquote）

### 警报（alert）

Alerts are an extension of the blockquote syntax that you can use to emphasize critical information. On GitHub, they are displayed with distinctive colors and icons to indicate the importance of the content. Alert syntax is supported in:

- Issues
- Pull requestes
- Markdown files
- Discussions
- Gists
- Wikis
- Releases

We recommend restricting the use of alerts to one or two per article to avoid overloading the reader. Consecutive alerts should be avoided.

Multiple types of alerts are available. You can add an alert with a special blockquote line that specifies the alert type, and then add the alert information in a standard blockquote immediately after.

```Markdown
> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.
```

> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.

### 代码块（fenced code block）

You can find out which keywords are valid in the [languages YAML file](https://github.com/github-linguist/linguist/blob/master/lib/linguist/languages.yml).

To display triple backticks in a fenced code block, wrap them inside quadruple backticks.

`````Markdown
````
```
Look! You can see my backticks.
```
````
`````

````Markdown
```
Look! You can see my backticks.
```
````

#### 示意图（diagram）

##### Mermaid

````Markdown
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

#### 地图（map）

##### GeoJSON

````Markdown
```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
              [-90,35],
              [-90,30],
              [-85,30],
              [-85,35],
              [-90,35]
          ]
        ]
      }
    }
  ]
}
```
````

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
              [-90,35],
              [-90,30],
              [-85,30],
              [-85,35],
              [-90,35]
          ]
        ]
      }
    }
  ]
}
```

##### TopoJSON

````Markdown
```topojson
{
  "type": "Topology",
  "transform": {
    "scale": [0.0005000500050005, 0.00010001000100010001],
    "translate": [100, 0]
  },
  "objects": {
    "example": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "properties": {"prop0": "value0"},
          "coordinates": [4000, 5000]
        },
        {
          "type": "LineString",
          "properties": {"prop0": "value0", "prop1": 0},
          "arcs": [0]
        },
        {
          "type": "Polygon",
          "properties": {"prop0": "value0",
            "prop1": {"this": "that"}
          },
          "arcs": [[1]]
        }
      ]
    }
  },
  "arcs": [[[4000, 0], [1999, 9999], [2000, -9999], [2000, 9999]],[[0, 0], [0, 9999], [2000, 0], [0, -9999], [-2000, 0]]]
}
```
````

```topojson
{
  "type": "Topology",
  "transform": {
    "scale": [0.0005000500050005, 0.00010001000100010001],
    "translate": [100, 0]
  },
  "objects": {
    "example": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "properties": {"prop0": "value0"},
          "coordinates": [4000, 5000]
        },
        {
          "type": "LineString",
          "properties": {"prop0": "value0", "prop1": 0},
          "arcs": [0]
        },
        {
          "type": "Polygon",
          "properties": {"prop0": "value0",
            "prop1": {"this": "that"}
          },
          "arcs": [[1]]
        }
      ]
    }
  },
  "arcs": [[[4000, 0], [1999, 9999], [2000, -9999], [2000, 9999]],[[0, 0], [0, 9999], [2000, 0], [0, -9999], [-2000, 0]]]
}
```

#### 交互式 3D 模型（interactive 3D model）

##### STL

````Markdown
```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```
````

```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```

### 注脚（footnote）

```Markdown
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.
```

Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.

The position of a footnote in your Markdown does not influence where the footnote will be rendered. You can write a footnote right after your reference to the footnote, and the footnote will still render at the bottom of the Markdown.

Footnotes are not supported in wikis.

### 折叠（collapse）

You can streamline your Markdown by creating a collapsed section with the `<details>` tag. Within the `<details>` block, use the `\<summary\>` tag to let readers know what is inside.

The details are shown when `open` attribute exists, or hidden when `open` attribute is absent.

```Markdown
<details>

<summary>Tips for collapsed sections</summary>

You can add a header

You can add text within a collapsed section. 

You can add an image or a code block, too.
</details>
```

<details>

<summary>Tips for collapsed sections</summary>

You can add a header

You can add text within a collapsed section. 

You can add an image or a code block, too.
</details>

### Mentioning people and teams

You can mention a person or team on GitHub by typing `@` plus their username or team name. This will trigger a notification and bring their attention to the conversation. People will also receive a notification if you edit a comment to mention their username or team name. For more information about notifications, see "About notifications."

> [!NOTE]
> A person will only be notified about a mention if the person has read access to the repository and, if the repository is owned by an organization, the person is a member of the organization.

```Markdown
@jacksalad What do you think about these updates?
```

@jacksalad What do you think about these updates?

