### 添加 HTML 以显示导航栏

导航栏位于网页标题中的 `<nav>` 标签中。

找到 `<header>` 和 `</header>` 标签。

添加 `<nav>` 标签。

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 11, 13
------------------------------------------------------------

```
<header>
  <nav>
    
  </nav>
</header>
```

\--- /code ---

使用 `<div>` 来包含到其他页面的链接。

在 `<nav>` 标签内，添加一个新的 `<div>`。

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 12-14
-----------------------------------------------------------

```
<header>
  <nav>
    <div>

    </div>
  </nav>
</header>
```

\--- /code ---

添加 `<a>` 标签来创建每个页面的链接。

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 13-15
-----------------------------------------------------------

```
<header>
  <nav>
    <div>
      <a href="index.html">主页</a>
      <a href="wildlife.html">野生动物</a>
      <a href="climate.html">气候</a>
    </div>
  </nav>
</header>
```

\--- /code ---

向包含导航栏链接的 `<div>` 添加 `nav-items` 类属性。

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 12
--------------------------------------------------------

```
<header>
  <nav>
    <div class="nav-items">
      <a href="index.html">主页</a>
      <a href="wildlife.html">野生动物</a>
      <a href="climate.html">气候</a>
    </div>
  </nav>
</header>
```

\--- /code ---

### 为整个导航栏设置样式

打开 `style.css` 文件和 `nav` 元素选择器。

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 36
line_highlights:
-----------------------------------------------------

/\* 导航栏 \*/
nav {
padding: 0 15px;
height: 60px;
font-size: 22px;
display: flex;
justify-content: center;
align-items: center;
background-color: #33658A;
}

\--- /code ---

为 `nav-items` 类创建一个选择器来分隔链接。

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 49
line_highlights: 50-53
-----------------------------------------------------------

/\* 导航项 \*/
.nav-items {
display: flex;
gap: 100px;
}

\--- /code ---

### 链接样式

除了设置整个导航栏的样式外，你还可以设置单个链接的样式。

创建另一个选择器来设置 `nav-items` div 中每个 `<a>` 标签的样式。

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 55
line_highlights: 56-60
-----------------------------------------------------------

/\* 导航栏链接 \*/
.nav-items > a {
color: #55DDE0;
text-decoration: none;
transition: .4s ease-in-out;
}

\--- /code ---

添加一个选择器，当你将鼠标悬停在每个链接上时设置其样式。

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 62
line_highlights: 63-65
-----------------------------------------------------------

/\* 导航链接悬停 \*/
.nav-items > a:hover {
color: white;
}

\--- /code ---

### 创建活动状态链接

index.html 页面将首先被加载。

当该页面打开时，链接应保持白色并且不可点击。

为当前打开的页面的链接添加一个新的 `active` CSS类。

## --- code ---

language: css
filename: style.css
line_numbers: true
line_number_start: 67
line_highlights: 68-71
-----------------------------------------------------------

/\* 活动状态的导航栏 \*/
.nav-items .active {
color: white;
pointer-events: none;
}

\--- /code ---

打开 `index.html`。

将 `active` 类属性添加到 index.html `<a>` 标签。

## --- code ---

language: html
filename: index.html
line_numbers: true
line_number_start: 10
line_highlights: 13
--------------------------------------------------------

```
<header>
  <nav>
    <div class="nav-items">
      <a href="index.html" class="active">家</a>
      <a href="wildlife.html">野生动物</a>
      <a href="climate.html">气候</a>
    </div>
  </nav>
</header>
```

\--- /code ---
