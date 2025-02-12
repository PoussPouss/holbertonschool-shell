#                                                                                      Shell, init files, variables and expansions
##                                    The objective is to learn how to manipulate variables, extensions and initialization files in the Shell with several tasks to perform.

Taks 0 : Create a script that creates an alias.
Name: ls
Value: rm -f *
===> alias ls="rm *"

Task 1 : Create a script that prints hello user, where user is the current Linux user.
===> echo hello $USER

Task 2 : Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
===> export PATH=$PATH:/action

Task 3 : Create a script that counts the number of directories in the PATH.
===> echo $PATH | tr  ':' '\n' | grep -c '^/'

Task 4 : Create a script that lists environment variables.
===> set

Task 5 : Create a script that lists all local variables and environment variables, and functions.
===> env | set  OR  set | grep -v BASH_EXECUTION_STRING | grep -v BASH_ARGV | head -2

Task 6 : Create a script that creates a new local variable.
Name: BEST
Value: School
===> BEST=School

Task 7 : Create a script that creates a new global variable.
Name: BEST
Value: School
===> export BEST=School

Task 8 : Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
===> echo $((${TRUEKNOWLEDGE} + 128))

Task 9 : Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.
POWER and DIVIDE are environment variables
===> echo $(($POWER/$DIVIDE))

Task 10 : Write a script that displays the result of BREATH to the power LOVE
BREATH and LOVE are environment variables
The script should display the result, followed by a new line
===> echo $(($BREATH**$LOVE))

Task 11 : Write a script that converts a number from base 2 to base 10.
The number in base 2 is stored in the environment variable BINARY
The script should display the number in base 10, followed by a new line
===> echo $((2#$BINARY))

Task 12 : Create a script that prints all possible combinations of two letters, except oo.
Letters are lower cases, from a to z
One combination per line
The output should be alpha ordered, starting with aa
Do not print oo
Your script file should contain maximum 64 characters
===> echo {a..z}{a..z} | tr ' ' '\n' | grep -v oo

Task 13 : Write a script that prints a number with two decimal places, followed by a new line.
The number will be stored in the environment variable NUM.
===> printf "%.2f\n" $NUM

Task 14 : Write a script that converts a number from base 10 to base 16.
The number in base 10 is stored in the environment variable DECIMAL
The script should display the number in base 16, followed by a new line
===> printf "%x\n" $DECIMAL
