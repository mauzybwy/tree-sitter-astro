# tree-sitter-astro

Tree-sitter grammar for the Astro web framework.

## Specification

This parser just uses the general idea that the document looks like
<pre><code>---
<i>{typescript}</i>
---
<i>{html}</i>
</pre></code>

and is essentially [tree-sitter-html](https://github.com/tree-sitter/tree-sitter-html) plus a snazzy way to write a `<script>` tag at the start of a document.

## Missing Features

Currently, the parser does not highlight code inside curly braces, e.g.
```astro
<ul>
  {items.map((item) => (
    <li>{item}</li>
  ))}
</ul>
```

does not highlight correctly.
