# cow cheatsheet

## Inputs & outputs

Moo
If current memory block == 0, read a single ASCII character from STDIN and store it in the current memory block.
If the current memory block =/= 0, then print the ASCII character that corresponds to the value in the current memory block to STDOUT.

oom
Read an integer from STDIN and put it into the current memory block.

OOM
Print value of current memory block (integer)

## Memory location

mOo
Lower position

moO
Increase position

## Values

MOo
Lower value

MoO
Increase value

OOO
Initialise value (0)

## Undefined

MMM
If no current value in register, copy current memory block value. If there is a value in the register, then paste that value into the current memory block and clear the register.

MOO
If current memory block value is 0, skip next command and resume execution after the next matching moo command. If current memory block value is not 0, then continue with next command. Note that the fact that it skips the command immediately following it has interesting ramifications for where the matching moo command really is. For example, the following will match the second and not the first moo: OOO MOO moo moo
