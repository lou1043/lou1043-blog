---
title: Structure of Code Block
date: 2022-10-20
draft: false
tags: [org]
categories: [org-mode]
author: "lou1043"
---



## Structure of Code Blocks {#structure-of-code-blocks}

Org offers two ways to structure source code in Org documents: in a source code block, and directly inline. Both specifications are shown below.

```org
#+NAME: <name>
#+BEGIN_SRC <language> <switched> <header arguments>
    <body>
#+END_SRC
```

Do not be put-off by having to remember the source block syntax. Org mode offers a commmand for warpping existing text in a block. Org also works with other completrion systems in Emacs, some of which predate Org and have custom domain-specific languages for defining templates. Regular use of templates reduces errors, increases accuracy, and maintains consistency.

An inline code block conforms to this structure:

```org
src_<language>{<body>}
```

or

```org
src_<language>[<header argument>]{<body>}
```


### '#+NAME: &lt;name&gt;' {#plus-name-name}

Optional. Names the source block so it can be called, like a function, from other source blocks or inline code to evaluate or capture the results. Code from other blocks, other files, and from table formulas can use the name to reference a source block. This naming servers the same purpose as naming Org tables. Org mode requires unique names. For duplicate names, Org mode's behavior is undefined.


### '#+BEGIN_SRC'...'#+END_SRC' {#plus-begin-src-dot-dot-dot-plus-end-src}

Mandatory. They mark the start and end of a block that Org requires. The '#+BEGIN+SRC' line takes additional arguments, as describe next.


### '&lt;language&gt;' {#language}

Mandatory. It is the identifier of the source code language in the block. See [Languages](https://orgmode.org/manual/Languages.html),for identifiers of supported languages.


### '&lt;switches&gt;' {#switches}

Optional. Switches provide finer control of the code execution, export, and format.


### '&lt;header arguments&gt;' {#header-arguments}

Optional. Heading arguments control many aspects of evaluation, export and tangling of code blocks. Using Org's properties feature, header arguments can be selectively applied to the entire buffer or specific sub-trees of the Org document.


### '&lt;body&gt;' {#body}

Source code in the dialect of the specified language identifier.
