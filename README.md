# ish-shell
### Overview
* program name : ish

### Building a Program
* use compiler options in the below
```bash
-D_BSD_SOURCE or -D_DEFAULT_SOURCE
-D_GNU_SOURCE
```

### Initialization and Termination
* Init
  * Read .ishrc file at $HOME dir
  * Print each line in .ishrc when reading  and executing .ishrc in format in the below
  > % LINE1
  > % LINE2
* Terminate program if user types Ctrl + d or when executing "exit" command
* **IMPORTANT**:
  > Program should handle exception when .ishrc file does not exist
     
### Functionalities to implement
1. print a prompt
   ```bash
   % PROMPT
   ```
2. Read a line from STDIN
3. Tokenize array of tokens
4. Check syntax of command
5. Execute command
  * Command list
    * setenv [var] [value] : if value is omitted, set empty string to [var]
    * unsetenv [var] : if var is not yet set, just ignore
    * cd [dir] : if dir is ommited, go to $HOME dir
    * exit : exit with status 0
  * **IMPORTANT**:
    > Print an error meesage if file redirection(e.g > ) is used with the above commands
  * Other cmd
    > If command contains code to be executed, execute command with **execvp** system call with all args.   
    > If there is eerro trying to execute command, print error message with reason for the failure   
       

### To get perfect grade
* Do not generate any warning message while compiling code with **gcc209**
* Follow <a href=https://ee209.kaist.ac.kr/style.pdf>coding style</a>
  > Names: You should use a clear and consistent style for variable and function names.   
  > One example of such a style is to prefix each variable name with characters   
  > that indicate its type. For example, the prefix c might indicate that the variable is of type char,   
  > i might indicate int, pc might mean char*, ui might mean unsigned int, etc.   
  > But it is fine to use another style -- a style which does not include the type of a variable in its name -- as long as the result is a readableprogram.   
   
### References
* <a href=https://ee209.kaist.ac.kr/assignments/assignment5/resource/dynarray.c>dynarray.c</a>
* <a href=https://ee209.kaist.ac.kr/assignments/assignment5/resource/dynarray.h>dynarray.h</a>
* <a href=https://ee209.kaist.ac.kr/assignments/assignment5/shellsupplementary.html>supplementary information</a>
