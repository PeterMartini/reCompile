# reCompile

A C++ library to generate native functions from regular expressions.

A regular expression is a string which express a pattern to use for
matching against other strings.  It generally will also allow captures,
which lets the user isolate one or more pieces of the string within
the pattern that they want to reference later.

In short, regular expressions are a programming language of their own.

This project treats them that way.  Our approach to handling regular
expressions is to treat them as a full programming language, first
parsing the string into an Abstract Syntax Tree, then breaking it into
blocks of code, then running regex specific optimization passes, against
the blocks, and finally running LLVMs JIT engine and optimization passes
to generate native code.
