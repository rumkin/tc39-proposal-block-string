# Block String

Add support of indentation string block to allow use a large block of strings into
the code without troubles with indentation.

Example:

```
  let markdownString = @ 
    There is a __string__ with several paragraphs

    Without quote escaping and so

  let ymlString = @
    base: element
    items:
      - item 1
      - item 2
  
  let htmlString = @
    <p>Good news everyone!</p>
  
  let page = 'Main';
  let jadeString = jade(@@ // with placeholders
    html
      head
        title {$page}
      body
        h1 Page
        p Hi block text
  );
```

This allow to avoid mess of quotation escaping and indentation for multiline strings.
So it allow to insert any other text inside js. Even js itself. Such string should get the first line
indentation and cut it from start of each following line.
