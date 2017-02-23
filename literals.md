# Literals

 *  Strings:
    
    ````kawaii
    var = 'string'              # Simple string.
    
    var = 'string `expression`' # Interpolated string.
    
    var = '
        miltiline
        string
    '                           # Multiline string
                                  with ignored
                                  indentations
                                  and start
                                  and end line breaks.
    
    var = 'string\ncontent'     # String with special
                                  character.
    
    var = @'string\ncontent'    # Raw string.
    
    var = @'
        multiline
        string
    '                           # Multiline string
                                  with included
                                  indentations.
    
    var = '\x12\u1234'          # String with ASCII
                                  and Unicode
                                  characters.
    ````
 *  Numbers:
     *  `1` — unsigned, 1 byte.
     *  `1U8` — unsigned, 1 byte,
        explicit type declaration.
     *  `1U16` — unsigned, 2 bytes.
     *  `1U32` — unsigned, 4 bytes.
     *  `1U64` — unsigned, 8 bytes.
     *  `1U128` — unsigned, 16 bytes.
     *  `1S8` — signed, 1 byte.
     *  `1S16` — signed, 2 bytes.
     *  `1S32` — signed, 4 bytes.
     *  `1S64` — signed, 8 bytes.
     *  `1S128` — signed, 16 bytes.
     *  `1.0` — floating-point, 4 bytes,
        implicit type inference.
     *  `1F32` — floating-point, 4 bytes,
        explicit type declaration.
     *  `1F64` — floating-point, 8 bytes,
        explicit type declaration.
     *  `1F128` — floating-point, 16 bytes,
        explicit type declaration.
     *  `0h01` — unsigned, hexadecimal.
     *  `0o01` — unsigned, octal.
     *  `0b01` — unsigned, binary.
     *  `0b10.01` — floating-point, binary.
     *  `1e2` — unsigned, 1 byte, scientific notation.
     *  `0h1.1e2U128` — hexadecimal, unsigned, 16 bytes,
        scientific notation.
 *  Regular expressions:
     *  `//` — empty RegExp.
     *  `/a/` — RegExp (matches *a*).
     *  `/a/i` — RegExp with flags
        (matches both *`'A'`* and *`'a'`*).
     *  Multiline RegExp:
        
        ````
        var = /
            a
            |
            b
        /i
        ````
        Matches both *`'A'`*, *`'a'`*, *`'B'`* and *`'b'`*.
        All whitespaces, indents and line breaks
        are ignored in regular expressions.
     *  `@/ a | b /` — matches *`' a '`* or *`' b '`*.
 *  Lists:
     *  `expression1, expression2` — list with two items.
     *  Multiline list literal:
        
        ````kawaii
        var =
            expression1,
            expression2,
        ````
        Please note, that ending comma,
        which are not required, but strongly recommended
        in multiline list literals.
 *  Vectors:
     *  `expression1 expression2` — two-dimensional vector.
     *  Multiline two-dimensional vector:
        
        ````kawaii
        var =
            expression1
            expression2
        ````
 *  Objects:
     *  Object literal:
        
        ````kawaii
        var =
            field1 = expression1
            field2 = expression2
        ````
