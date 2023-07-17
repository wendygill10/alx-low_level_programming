A struct in the C programming language (and many derivatives) is a composite data type (or record) declaration that defines a physically grouped list of variables under one name in a block of memory, allowing the different variables to be accessed via a single pointer or by the struct declared name which returns the same address. The struct data type can contain other data types so is used for mixed-data-type records such as a hard-drive directory entry (file length, name, extension, physical address, etc.), or other mixed-type records (name, address, telephone, balance, etc.).

The C struct directly references a contiguous block of physical memory, usually delimited (sized) by word-length boundaries. It corresponds to the similarly named feature available in some assemblers for Intel processors. Being a block of contiguous memory, each field within a struct is located at a certain fixed offset from the start.

Because the contents of a struct are stored in contiguous memory, the sizeof operator must be used to get the number of bytes needed to store a particular type of struct, just as it can be used for primitives. The alignment of particular fields in the struct (with respect to word boundaries) is implementation-specific and may include padding, although modern compilers typically support the #pragma pack directive, which changes the size in bytes used for alignment.

0. Poppy
Define a new type struct dog with the following elements:

name, type = char *

age, type = float

owner, type = char *

1. A dog is the only thing on earth that loves you more than you love yourself
Write a function that initialize a variable of type struct dog

Prototype: void init_dog(struct dog *d, char *name, float age, char *owner);

2. A dog will teach you unconditional love. If you can have that in your life, things won't be too bad
Write a function that prints a struct dog

Prototype: void print_dog(struct dog *d);

Format: see example bellow

You are allowed to use the standard library

If an element of d is NULL, print (nil) instead of this element. (if name is NULL, print Name: (nil))

If d is NULL print nothing.

3. Outside of a dog, a book is a man's best friend. Inside of a dog it's too dark to read
Define a new type dog_t as a new name for the type struct dog.
4. A door is what a dog is perpetually on the wrong side of
Write a function that creates a new dog.

Prototype: dog_t *new_dog(char *name, float age, char *owner);

You have to store a copy of name and owner

Return NULL if the function fails

5. How many legs does a dog have if you call his tail a leg? Four. Saying that a tail is a leg doesn't make it a leg
Write a function that frees dogs.

Prototype: void free_dog(dog_t *d);

