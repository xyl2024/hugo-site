---
author: Hugo Authors
title: 数学排版
date: 2019-03-08
description: KaTeX设置简要指南
math: true
draft: true
---

Hugo项目中的数学符号可以通过使用第三方JavaScript库来启用。
<!--more-->

在这个例子中，我们将使用 [KaTeX](https://katex.org/)。


- 在`/layouts/partials/math.html`下创建一个部分
- 在这个部分引用中，[自动渲染扩展](https://katex.org/docs/autorender.html)或本地托管这些脚本。
- 在模板中包含部分，如下所示： 

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```
- 要在全局启用KaTeX，请在项目的配置中将参数`math`设置为`true`。
- 要在每页的基础上启用KaTeX，请在内容文件中包含参数`math：true`。

**注意**：使用[支持的TeX函数](https://katex.org/docs/supported.html)在线参考。

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css" integrity="sha384-n8MVd4RsNIU0tAv4ct0nTaAbDJwPJzDEaqSD1odI+WdtXRGWt2kTvGFasHpSy3SV" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js" integrity="sha384-XjKyOOlGwcjNTAIQHIpgOno0Hl1YQqzUOEleOLALmuqehneUG+vnGctmUb0ZY0l8" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### 例子

行内数学公式：$\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…$

块数学公式：
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
