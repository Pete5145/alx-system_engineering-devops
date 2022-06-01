**This script creates an alias ** 0-alias
#!/bin/bash
alias ls="rm *"

**This script prints hello user, where user is the current LINUX user** 1-hello_you
#!/bin/bash
echo hello $USER

**This script adds /action to the PATH. /action should be the last directory the shell looks into when looking for a program** 2-path
#!/bin/bash
PATH="$PATH:/action"

**This script counts the number of directories in the PATH** 3-paths
#!/bin/bash
echo $PATH | tr ':' '\n' | wc -l

**This script list environment variables ** 4-global_variables
#!/bin/bash
printenv

**This script lists all local variables and environment variables, and functions** 5-local_variables
#!/bin/bash
set

**This script creates a local variable** 6-create_local_variable
#!/bin/bash 
BEST='School'

**This script creates a new Global variable** 7-create_global_variable
#!/bin/bash
export BEST='School'

**This script prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.** 8-true_knowledge
type export TRUEKNOWLEDGE=1209 in the shell
#!/bin/bash
echo $((128 + TRUEKNOWLEDGE))

**This script prints the result of POWER divided by DIVIDE, followed by a new line.** 9-divide_and_rule
type export POWER=42784 and export DIVIDE=32 in the shell
#!bin/bash
echo $(($POWER / $DIVIDE))

**This script displays the result of BREATH to the power LOVE** 10-love_exponent_breath
type export BREATH=4 and export LOVE=3 in the shell 
#!/bin/bash
echo $(($BREATH ** $LOVE))

**This script converts a number from base 2 to base 10.** 11-binary_to_decimal
type export BINARY=10100111001 in the shell
#!/bin/bash
echo $((2#$BINARY))

**This script prints all possible combinations of two letters, except oo.** 12-combinations
#!/bin/bash
echo {a..z} {a..z} | tr ' ' '\n' | grep -v "oo"

**This script prints a number with two decimal places, followed by a new line** 13-print_float
Create global variables
type export NUM=0 in the shell
#!/bin/bash
printf '%.2f\n' $NUM

**This script converts a number from base 10 to base 16.** 100-decimal_to_hexadecimal
Create global variables
type export DECIMAL=16, export DECIMAL=1337 and export DECIMAL=15 in the shell
#!/bin/bash
printf '%x\n' $DECIMAL

**This script encodes and decodes text using the rot13 encryption. Assume ASCII.** 101-rot13
#!/bin/bash
tr 'A-Ma-mN-Zn-z' 'N-Zn-zA-Ma-m'

**This script prints every other line from the input, starting with the first line.** 102-odd
#!/bin/bash
paste -- | cut -f1

**This script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.** 103-water_and_stir
type export WATER="ewwatratewa", export STIR="ti.itirtrtr" in the shell
#!/bin/bash
printf '%o\n'$((5#$(echo $WATER | tr water 01234) + 5#$(echo $STIR | tr stir. 01234) )) | tr 01234567 bestchol






