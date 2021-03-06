Standard C Syntax File
======================

This syntax file is to highlight Standard C source code, and can be confgured to
highlight to the C89, C94, or C99 standard. This syntax file is useful if you
are developing portable Standard C code, so that extensions that your compiler
supports (such as C++ `//` comments in C89) that may not be supported by another
compiler are flagged as errors. It is better to catch these problems at edit
time than from the overnight build. Additional non-standard C features can be
allowed - C++ comments, GNU C keywords, `$` in identitfiers for VMS C, etc. - for
when they are needed.

Highlighting features not in the standard VIM C syntax file:

* Function, variable, and macro identifier highlighting.
* Operator - math, pointer, logical, and bit - highlighting.
* Strict (almost) Standard C `printf()` and `scanf()` formatting - `"%s"` etc.
* Standard C reserved macro names - such as starting with `__` (double underscore).
* Highlighting of all syntax elements within macro definitions.
* Highlighting `0` (zero) integer constants as an octal number.

Highlighted errors:

* Invalid logical operators - `&&=` and `||=`.
* Undefined escaped characters - e.g. `\q`.
* Undefined string format specifiers - e.g. `"%m"`.
* Invalid octal numbers, as well as optionally all octal numbers to avoid any
  possible confusion - e.g. `0123`.
* Spaces after the line concatenation operator `\` in macro and string literal
  declarations.
* Trigraphs, so as to avoid unexpected character translations.
* Obscure invalid hex constant expression like `x = 0xE+y;`.

Information on how to configure and extend the syntax highlight file is included
in a help file that can be installed and accessed using VIM's normal help
commands.  Copy the doc and syntax directories into your local VIM runtime files
directory.
