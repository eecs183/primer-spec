---
layout: spec
latex: true
mermaid: true
authors:
  - Andrew DeOrio
  - Steven Bogaerts
ta_authors:
  - Sesh Sadasivam
  - Bella Kim
---

# EECS 183-specific Theme Features

The 183-specific additions to the theme are intended to reduce / eliminate duplication of text. Certain common text is provided in Markdown in the `_includes` directory and should be edited there, rather than copied into multiple webpages directly. I prefer writing in Markdown rather than HTML, so I made a `_includes/render_markdown.html` file that we should be able to include in any context, to properly render any markdown file. Some examples of how to use all this follow.

## Partner Policy

This is probably only appropriate for projects 3 and 4. Using the text in `_includes/partner.md`,

``` liquid
{% include render_markdown.html file="parter.md" %}
```

results in:

{% include render_markdown.html file="parter.md" %}

## Honor Code

This should probably be included in every project. Using the text in `_includes/honor_code.md`,

``` liquid
{% include render_markdown.html file="honor_code.md" %}
```

results in:

{% include render_markdown.html file="honor_code.md" %}

## Copyright Notice

Finally, `_includes/copyright.md` is loaded automatically on every page, as specified in `_layouts/spec.html`. You should see it directly below this final message. You can customize the names that appear using the YAML frontmatter tags `authors` and `ta_authors`. Each takes a list. For example, this very page includes the following YAML:

``` yaml
---
layout: spec
latex: true
mermaid: true
authors:
  - Andrew DeOrio
  - Steven Bogaerts
ta_authors:
  - Sesh Sadasivam
---
```

I believe that technically IAs and GSIs do "work for hire" and thus can't hold the copyright for items developed as part of their employment, hence the separate tag and wording.
