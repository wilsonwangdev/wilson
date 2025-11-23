# MISC

Q: What does misc mean?

A: It's an abbreviation, it's short for **misc**ellaneous, it's used to group things that are uncategoried temporarily.

Q: Why does C/C++ use & as the symbol of "address of"?

A: C uses ampersand for “address-of” largely because B did, and Ken Thompson felt “ampersand” sounded like “address.”

Q: What does * mean in C?

A: In C, the asterisk ‎`*` is a dereference operator, it means "go to the address in this pointer and access the value stored there"

> C inherited pointer concepts from B and BCPL. B used ‎`*` for indirection (dereference), influenced by earlier notations where a dot or other marks indicated indirection; ASCII availability and teletype constraints made ‎`*` a practical choice.

Q: What's the relation of & and *?

A: In C, & and * are opposites: & takes the address of a variable; * follows an address (pointer) to the value stored there.

> An address is a numeric location in memory; a pointer is a variable that stores such an address

Q: Why does C/C++ use # to include header files

A: C/C++ use # for preprocessor directives (like #include) because the C preprocessor is a separate, line-oriented phase that runs before compilation.

> The hash marks those lines as preprocessor commands to be handled by that tool, not by the C/C++ compiler. Historically this comes from early Unix C, which adopted a simple text macro processor modeled after CPP; # was chosen as an uncommon character to avoid clashes with normal code.
