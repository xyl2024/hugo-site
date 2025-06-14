+++
author = "Hugo Authors"
title = "Markdown 语法指南"
date = "2019-03-11"
description = "展示基本 Markdown 语法和 HTML 元素格式的示例文章。"
tags = [
    "markdown",
    "css",
    "html",
    "themes",
]
categories = [
    "themes",
    "syntax",
]
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
image = "pawel-czerwinski-8uZPynIu-rQ-unsplash.jpg"
draft = true
+++

本文提供了一个基本的 Markdown 语法示例，该示例可以在 Hugo 内容文件中使用，同时它还显示了基本 HTML 元素是否在 Hugo 主题中使用 CSS 进行装饰。
<!--more-->

## 标题

以下 HTML 元素 `<h1>`—`<h6>` 代表六个级别的章节标题。`<h1>` 是最高级别的章节，而`<h6>`是最低级别的章节。

# H1
## H2
### H3
#### H4
##### H5
###### H6

## 段落

Xerum，那些解释了痛苦和劳动的人。还有那些充满活力、追求快乐的人，他们是否也经历了痛苦和挣扎？有些人认为，幸福是通过努力和坚持获得的，而另一些人则认为，幸福是通过享受生活中的美好事物来实现的。那么，什么是真正的幸福呢？有些人认为，幸福是一种内在的感觉，而另一些人则认为，幸福是通过外部因素来实现的。那么，幸福到底是什么？有些人认为，幸福是一种选择，而另一些人则认为，幸福是通过努力和坚持来实现的。那么，幸福到底是什么？ 

## 引用

blockquote 元素表示从其他来源引用的内容，可选地带有引用，引用必须在`footer`或`cite`元素内，并且可选地带有注释和缩写等内联更改。 

#### 没有出处的引用

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.

#### 带有引用的块引用

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## 表格

表格不是核心 Markdown 规范的一部分，但Hugo支持开箱即用。

   Name | Age
--------|------
    Bob | 27
  Alice | 23

#### 表格内的内联Markdown

| Italics   | Bold     | Code   |
| --------  | -------- | ------ |
| *italics* | **bold** | `code` |

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------------|
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

## 代码块

#### 带有反引号的代码块

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```

#### 代码块缩进四个空格

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### 带有 Hugo 内部高亮简码的代码块
{{< highlight html >}}
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

#### 差异代码块

```diff
[dependencies.bevy]
git = "https://github.com/bevyengine/bevy"
rev = "11f52b8c72fc3a568e8bb4a4cd1f3eb025ac2e13"
- features = ["dynamic"]
+ features = ["jpeg", "dynamic"]
```

## 列表类型

#### 有序列表

1. 第一项
2. 第二项
3. 第三项

#### 无序列表

* 哈基米
* 米基哈

#### 嵌套列表

* 水果
  * 苹果🍎
  * 橙子🍊
  * 香蕉🍌
* 乳制品
  * 牛奶🥛
  * 奶酪🧀

## 其他元素 —— 缩写、下标、上标、键盘输入、标记

<abbr title="Graphics Interchange Format">GIF</abbr> 是一种位图图像格式。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按下 <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> 以结束会话。


大多数<mark>蝾螈</mark>是夜行动物，捕食昆虫、蠕虫和其他小型生物。 

## 超链接图像

[![Baidu](https://img.tukuppt.com/png_preview/00/10/46/IHk8cns6Re.jpg!/fw/780)](https://www.baidu.com)