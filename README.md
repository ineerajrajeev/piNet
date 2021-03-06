# piNet
## Translate Python Code to HTML

pieNet is a python module built to work with seamlessly Web Development frameworks like Django and Flask. This module renders Python code to HTML

## Features

- Compatible with Python 3
- Supports all tags and global attributes supported by HTML 5
- HTML files can either be rendered or can be exported from Python File
- Does not require any dependencies to be installed

## Installation

pieNet requires Python 3 to run so make sure you're using latest version of PIP and Python

```bash
pip install pienet
```

## Usage

```python
from pienet import *
obejct = html("Hello World") # Generates HTML object with 'Hello World' as Title
page_to_be_exported = object.render(
    object.h1(name="heading_1", id="heading_1", clas="heading_1").render(
        object.p(name="paragraph", id="paragraph", clas="paragraph").render(
            "Text in first Paragraph"
        ),
        object.a(href="https://any_link", target='_blank').render(
            object.p(name="paragraph", id="paragraph", clas="paragraph").render(
                "Text in Second Paragraph"
            )
        )
    )
)
export_html(page_to_be_exported, 'filename.html')
```

Above code generates a HTML file in current working directory named  ```filename.html```
The contnts of the file would be as follows

```
<!DOCTYPE html>
<html>
  <head>
    <title>Hello world</title>
  </head>
  <body>
    <h1 name="heading_1" id="heading_1" class="heading_1">
        <p name="paragraph" id="paragraph" class="paragraph">
            Text in first Paragraph
        </p>
        <a href="https://any_link" target="_blank">
            <p name="paragraph" id="paragraph" class="paragraph">
                Text in Second Paragraph
            </p>
        </a>
    </h1>
  </body>
</html>

```

## Bugs
Since module is still in Beta testing so few tags are yet to be added. Please let me knnow if you encounter any bug, crash, etc. or If you have any suggestion feel free to let me know.


## License

GNU General Public License
