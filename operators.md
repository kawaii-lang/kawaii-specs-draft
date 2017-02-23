# Operators

 *  `!` — negation.
     *  Arity: 1.
     *  Affix type: prefix.
     *  Associativity: RTL.
     *  Overloadable: yes.
     *  Scope:
         *  `Unsigned` — bitwise inverse.
         *  `Signed | Float` — additive inverse.
         *  `Boolean` — logical inverse.
         *  `List | String` — reverse order.
 *  `--` — decrement.
     *  Arity: 1.
     *  Affix type: prefix.
     *  Associativity: RTL.
     *  Overloadable: yes.
     *  Scope:
         *  `Number` — decrement by 1
            and return new value.
         *  `List | String` — remove first item
            and return it's value.
 *  `--` — decrement.
     *  Arity: 1.
     *  Affix type: postfix.
     *  Associativity: RTL.
     *  Overloadable: yes.
     *  Scope:
         *  `Number` — return old value,
            then decrement by 1.
         *  `List | String` — remove first item
            and return modified list.
 *  `++` — increment.
     *  Arity: 1.
     *  Affix type: prefix.
     *  Associativity: RTL.
     *  Overloadable: yes.
     *  Scope:
         *  `Number` — increment by 1
            and return new value.
         *  `List | String` — remove last item
            and return it's value.
 *  `++` — increment.
     *  Arity: 1.
     *  Affix type: postfix.
     *  Associativity: RTL.
     *  Overloadable: yes.
     *  Scope:
         *  `Number` — return old value,
            then increment by 1.
         *  `List | String` — remove last item
            and return modified list.
 *  `@` — raw literal.
     *  Arity: 1.
     *  Affix type: prefix.
     *  Associativity: N/A.
     *  Overloadable: no.
     *  Scope:
         *  Used for creating raw string literals.
         *  Used for creating RegExp with spaces
            and line breaks, parsed as part of expression.
 *  `@` — runtime annotation.
     *  Arity: 2.
     *  Affix type: prefix.
     *  Associativity: N/A.
     *  Overloadable: no.
     *  Scope:
         *  Used for annotating functions, classes,
            class members, constructs and aspects.
 *  `@@` — compile-time annotation.
     *  Arity: 2.
     *  Affix type: prefix.
     *  Associativity: N/A.
     *  Overloadable: no.
     *  Scope:
         *  Used for annotating entities
            with compile-time annotations.
