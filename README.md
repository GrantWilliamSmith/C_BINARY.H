# C_BINARY.H
C Macro Library that allows for a binary vs. standard hex. Useful for educational purposes such as teaching first time programmers without having to also teach hex, which can be complicated for a first time programmer in a classroom setting. This is not for real world application.

EG:
_0b00101001 vs. 41 vs. 0x29

Q: Why was this created?

A: When teaching kids programming (and I’m talking about kids grades 4 to 10) they have a hard enough time understanding binary for the first time, and hex just adds to the confusion. This library can be used to obfuscate the hex side of things and make setting particular bits easier.

Q: Why only make it for one byte?

A: Anything larger than 8 bits is not needed. I only teach kids to work with 8 bits at a time, since a lot of 16 bit microcontrollers have 8 bit registers, and any 16 bit operations (where supported) still move those bits only 1 byte at a time. So regardless of the endianness or ALU size the uC will often still move everything a single byte at a time. If you want more than 8 bits just pull up an excel sheet and add to this library, but I don’t recommend that you do that.

Q: Is this safe for production?

A: I don’t guarantee that this is but it’s probably safe considering that it’s a macro library and the compiler will just replate the macros with the desired numerical equivalent anyways. But I don’t recommend that this is used for anything other than educational proposes anyways, it’s cumbersome and will probably piss-off your boss. For teaching first time learners its great, for everything else just stick with hex. 

Q: Is this for real?

A: Yes, but try teaching a child binary and then hexadecimal in the same day and you’ll quickly realize why I made this library. It’s the lesser of two hassles. 
