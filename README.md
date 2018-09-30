---
title:  "readme"
---

This is the source for <https://koddo.github.io/test-jekyll-cayman-theme/>.

# Markdown

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

# Adding MathJax to pages

Usually we use layouts and front matter for having something enabled, but here we'd like to have the site generated by github and don't want to mess with the default layout.

So, just add `{% raw  %}{% include mathjax.html %}{% endraw  %}` at the top of the file and that's it.


