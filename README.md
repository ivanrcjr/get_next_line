<h1 align="center">
  📜 get_next_line 📜
</h1>

<p align="center">
  <b><i>Reading a line from a fd is way too tedious</i></b><br>
</p>

---

##  📚 About the project
> _This project is about programming a function that returns a line
read from a file descriptor._

    The get_next_line project is a fundamental exercise that challenges developers to create a
    function capable of reading a file line by line. In a broader context, this function becomes
    a crucial tool in handling input and output operations efficiently.

    Developers implementing get_next_line learn the intricacies of managing file descriptors, memory
    allocation, and buffer handling. This project delves into the heart of C programming, requiring
    a deep understanding of file I/O operations, dynamic memory allocation, and string manipulation.

    This function, when perfected, allows for seamless reading from multiple file descriptors
    simultaneously. It is an essential skill for anyone venturing into systems programming,
    file manipulation, or any domain where efficient text processing is paramount.

For more detailed information, check the [**subject of this project**](https://github.com/ircjr/get_next_line/blob/main/en.subject.pdf)

## 📖 Guide to get_next_line

### 1️⃣ Understanding the basics

A good start would be to know what a **static variable** is.

So what is a static variable?

Basically, a static variable is a variable that maintains its value between function calls, staying in memory throughout the program's execution. It is initialized only once and retains its value between calls, being accessible only within the scope of the function where it was declared.

For more detailed information, check the Wikipedia on [**static variable**](https://en.wikipedia.org/wiki/Static_variable)

Aqui temos um exemplo prático de como uma variável estática pode funcionar:

```
#include <stdio.h>

void	modify_str(void)
{
	static char	str[] = "Example";
	int			i;

	i = 0;
	while (str[i])
	{
		str[i] = 'X';
		printf("Modifying the position [%d]: %s\n", i, str);
		i++;
	}
}

int	main(void)
{
	modify_str();
	return (0);
}
```

A compilação e executação do código acima nos traz o incŕivel resultado:

```
Modifying the position [0]: Xxample
Modifying the position [1]: XXample
Modifying the position [2]: XXXmple
Modifying the position [3]: XXXXple
Modifying the position [4]: XXXXXle
Modifying the position [5]: XXXXXXe
Modifying the position [6]: XXXXXXX
```

## 📋 Testing

This command will compile your project and run the program, displaying the output with newline characters represented as **$**. Make sure to uncomment the main function in the [**get_next_line.c**](https://github.com/ircjr/get_next_line/blob/main/get_next_line.c) file before running and replace **<size>** with the desired buffer size.

```shell
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=<size> get_next_line.c get_next_line_utils.c && ./a.out | cat -e
```
The command remains the same for the bonus part of the project, just add the _bonus suffix to the source files.

```shell
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=<size> get_next_line_bonus.c get_next_line_utils_bonus.c && ./a.out | cat -e
```
