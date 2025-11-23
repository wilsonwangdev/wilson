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

Q: What's the difference between a reference and a pointer in C++?

A: A reference always refers to an object and can’t be reseated; a pointer holds an address, can be null, and can be reseated.

Q: What does common programming languages treat references and pointers?

A: In C++, both exist: references are non-null, non-reseatable aliases; pointers are addresses you can reseat, possibly null, with explicit dereference.

> C: Only pointers; no built-in references. Full manual control, pointer arithmetic allowed.
>
> Rust: Has safe references (‎`&T`, ‎`&mut T`) governed by the borrow checker and lifetimes, plus raw pointers (‎`*const/*mut T`) for unsafe code and FFI. No null for safe references; uses ‎`Option<&T>` for optionality.
>
> Java/C#: Only references to objects; no user-level pointer arithmetic. References can be null; memory is managed (GC). Value types behave differently (primitives in Java; structs in C#).
>
> Swift: Class instances are references with ARC; structs/enums are values. Unsafe pointer types exist (‎`UnsafePointer`) for low-level interop.
>
> Go: Has pointers but no arithmetic; garbage collection; many “reference-like” types (slices, maps, channels) that internally carry pointers.
>
> Python: Variables hold references to objects; everything is an object, and memory is managed. No explicit pointers.
>
> JavaScript: Primitives copy by value; objects/arrays/functions are passed and assigned by reference-like semantics. No explicit pointers.

Q: What does .a and .so mean in Linux?

A: .a means “archive” (static), .so means “shared object” (dynamic) from Unix/ELF history

> On Unix, static libraries were packaged by the ar tool into archives of object files, hence the extension .a for “archive.” Linkers would extract only needed objects from that archive at build time, embedding them into the executable.
>
> When System V and later Unix variants adopted ELF, they formalized dynamically loaded libraries as shared objects—ELF files with type ET_DYN—so the convention became .so for “shared object.”
