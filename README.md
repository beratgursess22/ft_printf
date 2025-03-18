# ft_printf
ft_printf  involves recreating the C standard printf function from scratch.

The goal of this project is to implement a function that behaves similarly to the standard printf, supporting various format specifiers.

ft_printf must support the following specifiers:

%c → Prints a single character.
%s → Prints a string.
%p → Prints a pointer address in hexadecimal format.
%d and %i → Prints a signed decimal (integer).
%u → Prints an unsigned decimal (integer).
%x and %X → Prints a number in lowercase (%x) or uppercase (%X) hexadecimal format.
%% → Prints a % character.

1-How ft_printf Works

Using Variadic Functions
Since printf can take a variable number of arguments, the stdarg.h library is used.
The macros va_list, va_start, va_arg, and va_end help manage these arguments dynamically.

2-Parsing the Format String

When ft_printf is called, it scans the provided format string (e.g., "Hello %s", "Value: %d").
It detects format specifiers marked by % and calls the corresponding function.

3-Handling Strings and Numbers

Strings and characters are printed directly.
Numbers are converted to strings using an itoa-like function before printing.
Hexadecimal and pointer formats require special conversion functions.
