# C Compilation Key Points

[reference](https://www.youtube.com/watch?v=ksJ9bdSX5Yo)

### Steps of Compilation

1. Preprocessor directives (#include, #define, #if) > source.i
2. Compilation "Proper" to machine or assembly > source.s
3. Assembler compiles / assembles the source into binary / object file > source.o
4. Linker brings in libraries statically (.o) or dynamically (.so) > program

### Static Linking

Statically linked libraries are loaded at compile time. They are compiled into the program.
Statically linked libraries are compiled by compiling the libraries together \
`gcc main.c lib.c`

You can also individually compile files to object files (.o): \
`// produces main.o, lib.o` \
`gcc -c main.c` \
`gcc -c lib.c` \
`// produces statically linked program` \
`gcc main.o lib.o` 

### Dynamic Linking

Dynamically linked libraries are loaded at runtime.
libraries are linked dynamically using the -l flag. \
`gcc main.c -lSDL2`

### Important flags

reference: man gcc

- [-o file] put output in specified output file
- [-c] compile and assemble source files, but do not link
- [-S] Stop after compilation proper (outputs assembly)
- [-E] Stop after preprocessing stage. Send result to stdout
- [-v] Print all commands executed to run compilation
- [-w] Do not show warning messages
- [-l{library}] Dynamically link library
- [-L{directory}] Add directory to compiler search for libraries 
- [-Wall] show all warnings
- [-Werror] make all warnings into errors

### Useful Commands

- objdump: Inspect source file
- ldd: Show linking of completed program
