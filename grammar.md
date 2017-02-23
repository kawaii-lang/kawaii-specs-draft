# Grammar

## Keywords

````
keyword =
    from   = 'from'
    import = 'import'
    as     = 'as'
````

## Other terminals

These terminals are described in RegExp-like style.
There are some additional wildcard characters:

 *  `\ii` — increase indent.
 *  `\ik` — keep current indentation level.
 *  `\id` — decrease indent.

````
terminal =
    whitespace = /^\ +/
    semicolon  = /^\;+/
    newline    = /^\n/

    indent =
        keep     = /^\ik/
        increase = /^\ii/
        decrease = /^\id/

    comment =
        start         = /^\#+/
        line          = /^[^\n]*/

    documentation =
        start = /^$+/

    identifier =
        type   = /[A-Z]\w*[a-z0-9]?/
        member = /[a-z]\w*[a-z0-9]?/
````

## Grammar

````
file =
    documentation?
    imports?
    body?

documentation =
    terminal.comment.documentation
    terminal.newline
    @terminal.indent.increase
    terminal.comment.line
    (
        terminal.newline
        terminal.indent.keep
        terminal.comment.line?
    )*
    separators.statement

separators.statement =
    terminal.newline
    terminal.indent.decrease

imports =
    import.statement+

import.statement =
    comment*
    (
        import.all | import.some
    )

comment =
    tokens.comment.general
    (
        terminal.whitespace
        terminal.comment.line
    )?
    (
        terminal.newline
        @terminal.indent.increase
        terminal.comment.line
        (
            terminal.newline
            terminal.indent.keep
            terminal.comment.line?
        )*
    )?

import.all =
    keyword.import
    terminal.whitespace
    package
    (
        terminal.whitespace?
        comment
    )?
````
