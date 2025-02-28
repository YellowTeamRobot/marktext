# MarkText

[MarkText](https://github.com/marktext/marktext) is a markdown editor written by [Jocs](https://github.com/Jocs) and [contributors](https://github.com/marktext/marktext/graphs/contributors).

This is a fork of [jacobwhall's MarkText repository](https://github.com/jacobwhall/marktext).

Build instructions can be found [here](https://github.com/YellowTeamRobot/marktext/blob/new2/docs/dev/BUILD.md)

## My changes

- [ ] Custom YAML frontmatter rendering with support for
  
  - [x] Export Render Support
  
  - [ ] WYSIWYG in-program Render Support
  
  - [ ] add styling to the frontmatter classes
  
  - `title:` which is converted to  `<h1>`  with class `frontmatter-title`
  
  - `subtitle:` which is converted to a div with class `frontmatter-subtitle`
  
  - `author:` which is converted to a div with class `frontmatter-author` will support multiple authors of form:
    
        author:
        - author one
        - author two
        - etc
  
  - `date:` in YYYY-MM-DD format  (converted to div with class `frontmatter-date`, will show in format `{LongMonthString} {DayNum}, {YYYY}` for example: `April 1, 2045`

- [ ] Custom multi-column blocks with support for markdown elements inside
  
  - [ ] implemented columns feature
  
  - [x] decided on scheme for the columns feature
    
    ```
     @startcolumns
    (0.4)
        ## markdown header
    
        markdown paragraph blah blah blah
    
        - markdown
        - list
        - with
        - multiple
        - elements
    (0.6)
        ## the second column
    
        has this markdown content
    
        a new paragraph
    
        | a | table |
        |---|-------|
        | h | hhhhh |
    @endcolumns
    ```
    
      will parse to
    
    ```html
    <div class="column-container" style="display:flex;">
      <div class="column-inner" style="flex:0.4;">
          <h2>markdown header</h2>
          <p>markdown paragraph blah blah blah</p>
          <ul>
              <li>markdown</li>
              <li>list</li>
              <li>with</li>
              <li>multiple</li>
              <li>elements</li>
          </ul>
      </div>
      <div class="column-inner" style="flex:0.6">
          <h2>the second column</h2>
          <p>has this markdown content</p>
          <p>a new paragraph</p>
          <table>
            <tr>
              <th>a</th>
              <th>table</th>
            </tr>
            <tr>
              <td>h</td>
              <td>hhhhh</td>
            </tr>
          </table>
      </div>
    </div>
    ```
    
      and display as
      ![Untitled](https://github.com/user-attachments/assets/42e0d8d3-4666-4536-803f-c47b9052b6fd)

- [ ] New theme: valve green

## License

MarkText uses the [MIT license](LICENSE).
