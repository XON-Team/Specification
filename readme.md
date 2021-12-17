# eXtensible Object Notation specification

## Purpose of XON
The XON Project exists to provide web developers a compact format in order to increase readaility, maintainability, and to decrease storage usage.

## Requirements of an XON Transpiler
1. Must be able to compile XON files to XML
2. Must be able to compile XML files to XON
3. Must provide insightful errors

## Requirements of the XON format
### 1. Document Type Definition (DTD)
The beginning of an XON file may include a DTD, which specifies the use of the file.
### 2. Tags
A tag is a string of characters, excluding white-space, that act as the name of the element.
  - Empty element tags must begin with `/`
### 3. Attributes
Attributes act as key-value pairs, defining data that the parser uses for the element.

### Example of an XON file with it's XML counterpart
XON:
```xon
!html
html {
  head {
    title "This is a title!"
  }
  body {
    div class="text" {
      p "Hello, world!"
    }
  }
}
```
XML:
```xml
<!doctype  html>
<html>
  <head>
    <title>This is a title!</title>
  </head>
  <body>
    <div class="text">
      <p>Hello, world!</p>
    </div>
  </body>
</html>
```
