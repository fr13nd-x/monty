# monty

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

##### Usage
monty file
where file is the path to the file containing Monty byte code

##### Files

push and pall - The opcode push pushes an element to the stack
``
Usage: push <int>
where <int> is an integer
if <int> is not an integer or if there is no argument given to push, print the error message L<line_number>: usage: push integer, followed by a new line, and exit with the status EXIT_FAILURE
where is the line number in the file``

pint - The opcode pint prints the value at the top of the stack, followed by a new line.
``Usage: pint
If the stack is empty, print the error message L<line_number>: can't pint, stack empty, followed by a new line, and exit with the status EXIT_FAILURE``

pop -  removes the top element of the stack.
``Usage: pop
If the stack is empty, print the error message L<line_number>: can't pop an empty stack, followed by a new line, and exit with the status EXIT_FAILURE``

swap -  swaps the top two elements of the stack.
``Usage: swap
If the stack contains less than two elements, print the error message L<line_number>: can't swap, stack too short, followed by a new line, and exit with the status EXIT_FAILURE
``
add -  adds the top two elements of the stack.
``Usage: add
If the stack contains less than two elements, print the error message L<line_number>: can't add, stack too short, followed by a new line, and exit with the status EXIT_FAILURE
The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
The top element of the stack contains the result
The stack is one element shorter``

nop - doesn’t do anything
``Usage: nop``

sub -  subtracts the top element of the stack from the second top element of the stack.

div - divides the second top element of the stack by the top element of the stack.

mul - multiplies the second top element of the stack with the top element of the stack.

mod - computes the rest of the division of the second top element of the stack by the top element of the stack.

pchar - prints the char at the top of the stack, followed by a new line.

pstr -  prints the string starting at the top of the stack, followed by a new line

rotl - rotates the stack to the top.

rotr - rotates the stack to the bottom.

stack -  sets the format of the data to a stack (LIFO). This is the default behavior of the program.

queue - sets the format of the data to a queue (FIFO).

bf - Brainfxck script that prints School, followed by a new line (mess up your brain huh)

1001-add.bf - Add two digits given by the user.

1002-mul.bf - Multiply two digits given by the user.
	``Read the two digits from stdin, multiply them, and print the result
The result of the multiplication will be one digit-long (<10)``

1003-mul.bf - Multiply two digits given by the user. 
	``Read the two digits from stdin, multiply them, and print the result, followed by a new line``
