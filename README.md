# MarkText

[MarkText](https://github.com/marktext/marktext) is a markdown editor written by [Jocs](https://github.com/Jocs) and [contributors](https://github.com/marktext/marktext/graphs/contributors).

This is a fork of [jacobwhall's MarkText repository](https://github.com/jacobwhall/marktext).

## My changes

- [ ] Custom YAML frontmatter rendering with support for
  
  - [x] Export Render Support
  
  - [ ] WYSIWYG in-program Render Support
  
  - `title:` which is converted to both `<title>` and `<h1>` (header with class `frontmatter-title`)
  
  - `subtitle:` which is converted to a span with class `frontmatter-subtitle`
  
  - `author:` span with class `frontmatter-author` will support multiple authors of form:
    
        author:
        - author one
        - author two
        - etc
  
  - `date:` in YYYY-MM-DD format

- [ ] Custom multi-column blocks with support for markdown elements inside

- [ ] New theme: valve green

## License

MarkText uses the [MIT license](LICENSE).
