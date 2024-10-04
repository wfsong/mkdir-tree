# mkdir-tree

`mkdir-tree` is a cli tool that generates directory structures from various input formats. It's inspired by the `tree` command-line tool but focuses on creating directory structures rather than just displaying them.

## Features

- Create directory structures from text, JSON, XML, or HTML input
- Simple command-line interface
- No external dependencies - just Python standard library

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/mkdir-tree.git
   cd mkdir-tree
   ```

2. Make the script executable:
   ```
   chmod +x mkdir-tree.py
   ```

3. (Optional) Add the script to your PATH or create an alias in your shell configuration file (e.g., `.zshrc`):
   ```
   alias mkdir-tree='python /path/to/mkdir-tree.py'
   ```

## Usage

```
python mkdir-tree.py [-f {text,json,xml,html}] input_file
```

Options:
- `-f`, `--format`: Specify the input file format (default: text)
- `input_file`: Path to the input file containing the directory structure

## Input Formats

### Text

A simple indented text format:

```
project/
    src/
        main.py
        utils.py
    docs/
        readme.md
    tests/
        test_main.py
```

### JSON

A JSON object representing the directory structure:

```json
{
  "project": {
    "src": {
      "main.py": null,
      "utils.py": null
    },
    "docs": {
      "readme.md": null
    },
    "tests": {
      "test_main.py": null
    }
  }
}
```

### XML

An XML representation of the directory structure:

```xml
<project>
  <src>
    <main.py/>
    <utils.py/>
  </src>
  <docs>
    <readme.md/>
  </docs>
  <tests>
    <test_main.py/>
  </tests>
</project>
```

### HTML

An HTML unordered list representing the directory structure:

```html
<ul>
  <li>project
    <ul>
      <li>src
        <ul>
          <li>main.py</li>
          <li>utils.py</li>
        </ul>
      </li>
      <li>docs
        <ul>
          <li>readme.md</li>
        </ul>
      </li>
      <li>tests
        <ul>
          <li>test_main.py</li>
        </ul>
      </li>
    </ul>
  </li>
</ul>
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.