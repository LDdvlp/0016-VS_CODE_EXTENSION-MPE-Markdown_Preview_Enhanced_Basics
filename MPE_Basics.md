|*Doc. #*|*Rédacteur*|*Création*|*Mise à jour*|
|:---:|:---:|---:|:---|
|***0016***|*Loïc Drouet*|_Mercredi 28 juin 2023_|_Vendredi 07 juillet 2023_|

# [MPE Basics - Markdown Preview Enhanced Basics](https://shd101wyy.github.io/markdown-preview-enhanced/#/markdown-basics)

# [MkDocs](https://www.mkdocs.org/)


## 1. Syntax guide

---

### Headers

```markdown
# This is an <h1> tag

## This is an <h2> tag

### This is an <h3> tag

#### This is an <h4> tag

##### This is an <h5> tag

###### This is an <h6> tag
```


# This is an \<h1> tag

## This is an \<h2> tag

### This is an \<h3> tag

#### This is an \<h4> tag

##### This is an \<h5> tag

###### This is an \<h6> tag

---

###  A MPE extended feature

```markdown
# This heading has 1 id {#my_id}

# This heading has 2 classes {.class1 .class2}
```

# This heading has 1 id {#my_id}

# This heading has 2 classes {.class1 .class2}

---

### Emphasis

```markdown
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

~~This text will be strikethrough~~
```

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_

~~This text will be strikethrough~~

---

### Lists

#### Unordered List

```markdown
- Item 1
- Item 2
  - Item 2a
  - Item 2b
```

- Item 1
- Item 2
  - Item 2a
  - Item 2b


#### Ordered List

```markdown
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

---

### Images

```markdown
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)
```

![GitHub Logo](/images/logo.svg.png)

---

### Links

```markdown
https://github.com - automatic!
[GitHub](https://github.com)
```

https://github.com - automatic!
[GitHub](https://github.com)

---

### Blockquote

```markdown
As Kanye West said:

> We're living the future so
> the present is our past.
```

As Kanye West said:

> We're living the future so
> the present is our past.

---

### Horizontal Rule

```markdown
Three or more...

---

Hyphens

---

Asterisks

---

Underscores

```

Three or more...

---

Hyphens

---

Asterisks

---

Underscores

---

### Inline code

```markdown
I think you should use an
`<addr>` element here instead.
```

I think you should use an
`<addr>` element here instead.


---

### Fenced code block


```markdown
You can create fenced code blocks by placing triple backticks ``` before and after the code block.
```

You can create fenced code blocks by placing triple backticks ``` before and after the code block.

#### Syntax Highlighting

You can add an optional language identifier to enable syntax highlighting in your fenced code block.

For example, to syntax highlight Ruby code:

```markdown
    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```
```

```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
```

---

### Code block class (MPE extended feature)

You can set `class` for your code blocks.

For example, to add `class1` `class2` to a code block

```markdown
    ```javascript {.class1 .class}
    function add(x, y) {
      return x + y
    }
    ```
```

#### line-numbers

You can enable `line-numbers` for a code block by adding line-numbers class.

For example:

```markdown
    ```javascript {.line-numbers}
    function add(x, y) {
      return x + y;
    }
    ```
```

```javascript {.line-numbers}
function add(x, y) {
  return x + y;
}
```

#### highlighting rows

You can highlight rows by add `highlight` attribute:

```markdown
    ```javascript {highlight=10}
    ```

    ```javascript {highlight=10-20}
    ```

    ```javascript {highlight=[1-10,15,20-22]}
    ```

    ```javascript {highlight=10}
    ```
```

#### Example JS with line numbers and some highlighted lines 

```javascript {.line-numbers highlight=[3-5,9-11,15-17, 21-23,27-29]}

// Addition code : The addition operator (+) adds numbers:

var x = 5;
var y = 5;
var z = x + y;

// Subtraction code: The subtraction operator (-) subtracts numbers.

var x = 10;
var y = 5;
var z = x - y;

// Multiplication code: The multiplication operator (*) multiplies numbers.

var x = 5;
var y = 2;
var z = x * y;

// Division code: The division operator (/) divides numbers.

var x = 10;
var y = 2;
var z = x / y;

// Modulus code: The modulus operator (%) returns the remainder of a number divided by

var x = 10;
var y = 2;
var z = x % y;

```

---

### Task lists 

```markdown
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

---

### Tables

```markdown
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

|First Header|Second Header|Third Header|
|:---|:---:|---:|
|Content from cell 1|Content from cell 2|Content from cell 3|
|Content in the first column|Content in the second column|Content in the third column|

```

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

|First Header|Second Header|Third Header|
|:---|:---:|---:|
|Content from cell 1|Content from cell 2|Content from cell 3|
|Content in the first column|Content in the second column|Content in the third column|

---

### Extended syntax

#### Table 

!!! warning
    Need to enable `enableExtendedTableSyntax` in extension settings to get it work !

```markdown
- colspan `>` or `empty cell`

|A|B|
|---|---|
|>|1|
|2||
||3|
|4|5|
|6|>|
||7|

- rowspan `^`

|A|B|
|---|---|
|1|2|
|^|3|
|4|5|
|6|^|

- colspan and rowspan

|A|B|C|
|---|---|---|
|1|2|3|
|4||5|
||6|7|
|8|^|9|
|0|||
```

- colspan `>` or `empty cell`

|A|B|
|---|---|
|>|1|
|2||
||3|
|4|5|
|6|>|
||7|

- rowspan `^`

|A|B|
|---|---|
|1|2|
|^|3|
|4|5|
|6|^|

- colspan and rowspan

|A|B|C|
|---|---|---|
|1|2|3|
|4||5|
||6|7|
|8|^|9|
|0|||

---

### Emoji & Font-Awesome

!!! warning
    This only works for markdown-it parser but not pandoc parser.
    Enabled by default. You can disable it from the package settings.

```markdown
:smile:
:fa-car:
```
:smile:
:fa-car:

---

### Superscript

```markdown
30^th^
```

30^th^

---

### Subscript

```markdown
H~2~O
```

H~2~O

---

### Footnotes

```markdown
Content [^1]

[^1]: Hi! This is a footnote
```


Content [^1]
(go to bottom for footnote)

[^1]: Hi! This is a footnote

---

### Abbreviation

```markdown
*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
The HTML specification
is maintained by the W3C.
```

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
The HTML specification
is maintained by the W3C.

---

### Mark

```markdown
==marked==
```

==marked==

---

### CriticMarkup

!!! warning
    CriticMarkup is **disabled** by default, but you can enable it from the package settings.
    CriticMarkup only works with the markdown-it parser, but not the pandoc parser.
    For more information about CriticMarkup, check [CriticMarkup User's Guide](https://criticmarkup.com/users-guide.php).

    [CriticMarkup / **CriticMarkup-toolkit**](https://github.com/CriticMarkup/CriticMarkup-toolkit)
    [CriticMarkup](https://fletcher.github.io/MultiMarkdown-6/syntax/critic.html)

There are five types of Critic marks:

```markdown
1. Addition `{++ ++}`
This {++is ++}a test.

2. Deletion `{-- --}`
This is {--is --}a test.

3.  Substitution `{~~ ~> ~~}`
This {~~isn't~>is~~} a test.

4. Comment `{>> <<}`
This is a test{>>What is it a test of?<<}.

5. Highlight `{== ==}{>> <<}`
This is a {==test==}.
```

1. Addition `{++ ++}`
This {++is ++}a test.

2. Deletion `{-- --}`
This is {--is --}a test.

3.  Substitution `{~~ ~> ~~}`
This {~~isn't~>is~~} a test.

4. Comment `{>> <<}`
This is a test{>>What is it a test of?<<}.

5. Highlight `{== ==}{>> <<}`
This is a {==test==}.

---

### Admonition

https://squidfunk.github.io/mkdocs-material/reference/admonitions/



```markdown
!!! note

    Text ...
```

!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! abstract

    Text ...
```

!!! abstract

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! info

    Text ...
```

!!! info

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! tip

    Text ...
```

!!! tip

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! success

    Text ...
```

!!! success

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! question

    Text ...
```

!!! question

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! warning

    Text ...
```

!!! warning

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! failure

    Text ...
```

!!! failure

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! danger

    Text ...
```

!!! danger

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! Bug

    Text ...
```

!!! Bug

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! example

    Text ...
```

!!! example

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! quote

    Text ...
```

!!! quote

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! note "Changing the title"

    Text ...
```

!!! note "Changing the title"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

```markdown
!!! note ""

    Text ...
```

!!! note ""

    "___Removing the title___"
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

## 2. Chunks

!!! warning You must enable script execution to run chunks. [^2]
    
    Script execution is off by default and needs to be explicitly enabled in VSCode extension preferences.
    Please use this feature with caution because it may put your security at risk.
    Your machine can get hacked if someone makes you open a markdown with malicious code while script execution is enabled.
    
    **Option name :** `enableScriptExecution`

[^2]: *Source : [https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/code-chunk.md](https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/code-chunk.md)*

!!! success Run PHP chunks.
    You must have defined the PHP path for the variable "Path" in Windows User Environment Variables.

## 3. Markdown cheatsheet

This is a quick reference cheat sheet to the Markdown syntax.

*Source : [https://quickref.me/markdown](https://quickref.me/markdown)*

## Markdown Quick Reference

### 1. Headers

#### 1.1 Headers (atx style)

ATX also works for all levels, while Setex only goes up to level 2.

*[https://arcticicestudio.github.io/styleguide-markdown/rules/headings.html#atx-style](https://arcticicestudio.github.io/styleguide-markdown/rules/headings.html#atx-style)*

*[http://www.aaronsw.com/2002/atx/intro](http://www.aaronsw.com/2002/atx/intro)*

*[https://docutils.sourceforge.io/mirror/setext.html](https://docutils.sourceforge.io/mirror/setext.html)*

        # h1
# h1

        # h2
## h2

        # h3
### h3

        # h4
#### h4

        # h5
##### h5

        # h6
###### h6

#### 1.2 Headers (setext style)

        Header 1
        ========

Header 1
========

        Header 2
        ========

Header 2
--------

---

### 2. Blockquotes

        > This is
        > a blockquote
        >
        > > Nested
        > > Blockquote

> This is
> a blockquote
>
> > Nested
> > Blockquote

---

### 3. Unordered List

        * Item 1
        * Item 2
            * item 3a
            * item 3b

* Item 1
* Item 2
    * item 3a
    * item 3b

**or**

        - Item 1
        - Item 2

- Item 1
- Item 2


**or**

        + Item 1
        + Item 2

+ Item 1
+ Item 2

**or**

```
    - [ ] Checkbox off
    - [x] Checkbox on
```

- [ ] Checkbox off
- [x] Checkbox on

---

### 4. Ordered List

        1. Item 1
        2. Item 2
            a. item 3a
            b. item 3b

1. Item 1
2. Item 2
    a. item 3a
    b. item 3b

---

### 5. Links

        [link](http://google.com)
[link](http://google.com)

        [link][google]

        [google]: http://google.com

[link][google]

[google]: http://google.com

        <http://google.com>

<http://google.com>

---

### 6. Emphasis

        *italic*
*italic*
        
        _italic_
_italic_

        **bold**
**bold**

        __bold__
__bold__

        `inline code`
`inline code`

        ~~struck out~~
~~struck out~~

---

### 7. Horizontal line

Hyphens

        ---
---

Asterisks

        ***

***

Underscores

        ___

___

---

### 8. Code

#### 8.1 Block Code

        ```javascript
        console.log("This is a block code")
        ```

```javascript
console.log("This is a block code")
```

        ~~~css
        .button { border: none; }
        ~~~

~~~css
.button { border: none; }
~~~

        4 space indent makes a code block

    4 space indent makes a code block

#### 8.2 Inline Code

        `Inline code` has back-ticks around it

`Inline code` has back-ticks around it

### 9. Tables

#### 9.1 Table

        | Left column | Center column | Right column |
        |:------------|:-------------:|-------------:|
        | Cell 1      |   Centered    |        $1600 |
        | Cell 2      |    Cell 3     |          $12 |

| Left column | Center column | Right column |
|:------------|:-------------:|-------------:|
| Cell 1      |   Centered    |        $1600 |
| Cell 2      |    Cell 3     |          $12 |

#### 9.2 Simple style


        Left column | Center column | Right column
        :----------:|:-------------:|:-----------:
           Cell 1   |   Centered    |    $1600
           Cell 2   |    Cell 3     |     $12

Left column | Center column | Right column
:----------:|:-------------:|:-----------:
   Cell 1   |   Centered    |    $1600
   Cell 2   |    Cell 3     |     $12


A markdown table generator : [https://tableconvert.com/](https://tableconvert.com/)

### 10. Images

#### 10.1 Image

        ![Alt Text](url)

        ![GitHub Logo](/images/logo.png)

![GitHub Logo](/images/logo.png)

#### 10.2 Image with link

        [![Alt Text](image_url)](link_url)

        [![GitHub Logo](/images/logo.png)](https://github.com/)

[![GitHub Logo](/images/logo.png)](https://github.com/)

#### 10.3 Reference style

        ![Alt Text][logo]

        [logo]: /images/logo.png "Logo Title"

![Alt Text][logo]

[logo]: /images/logo.png "Logo Title"
