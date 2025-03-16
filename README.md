# RMD (Rich Markdown)

>The latest version of RMD is currently b0.2. This documentation is up-to-date.

RMD (Rich Markdown) is a custom text formatting language inspired by Markdown, with additional rich text features and a structured syntax, while keeping it human-readable.

## Syntax

### Headings

```
\h1{Heading 1}
\h2{Heading 2}
\h3{Heading 3}
```

### Inline Formatting

| Format       | Syntax               | Example                | Rendered Output |
|-------------|----------------------|------------------------|----------------|
| Bold        | `\b{text}`           | `\b{bold text}`       | **bold text** |
| Italics     | `\i{text}`           | `\i{italic text}`     | *italic text* |
| Underline   | `\u{text}`           | `\u{underlined text}` | u͟n͟d͟e͟r͟l͟i͟n͟e͟d͟ t͟e͟x͟t͟ |

### Lists

RMD currently only supports numbered lists using `\list{}` syntax.

```
\list{1;"First item";2;"Second item";2.1;"Subitem";3;"Third item"}
```

### Links

```
\link{"Alt text";https://whalete.ch}
```

### Images

```
\img{"Alt text";https://example.com/image.png}
```

### Code Blocks

#### Inline Code:

```
\ic{inline code}
```

#### Block Code:

```
\cb{print("Hello, World!")
print("This is a code block")}
```

### Tabs

Tabs can be toggled using `\tabs{true/false}` at the start of the file. If `\tabs` is set to `true`, you can define tabs usign `\t#{` to start, and `\t#}` to end (with # representing the tab number). For example;

```
\tabs{true}
\t1{
text
\t1}
```

## Example Document

```
\tabs{true}

\t1{
\h1{Welcome to RMD}

This is a demonstration of RMD (Rich Markdown) formatted text.

\h2{Features}

\list{1;"Standard Markdown features";2;"Extended formatting using \b{}, \i{}, and \u{}";3;"Tables and horizontal rules are planned for future versions of the format."}

\h2{Code Example}

\cb{def hello():
    print("Hello, world!")}

\h2{Links and Images}

\link{"Visit whalete.ch";https://whalete.ch}

\img{"Example Image";https://example.com/image.png}
\t1}

\t2{
\h1{Tab 2}
\b{Tab 2 text}
\t2}
```
> A reader and editor is still being worked on.
