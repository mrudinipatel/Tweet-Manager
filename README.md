# Tweet-Manager 🐥

This project was created for CIS*2500.
Assignment #3: Dynamic Data Structures (linked lists) - Tweet Manager

## To Launch 🚀
```make```  
```./a3```  

The makefile links and compiles all source code files. The compilation rule consists of these flags: ```-std=c99 -Wall```.  

## Issues Encountered 🤺
The createTweet.c file has a section of code that validates the user's input. As I was attempting to validate the input so that it does not exceed the maximum byte size allocated by the struct in the headerA3.h file, I encountered an issue upon returning NULL, where the function looped over and over again.

Each loop cut the input string into smaller pieces until the input was entirely stored across multiple tweets. I wanted to return NULL in this case so that the function could return back to mainA3.c and the user will be repromted to select an option from the menu. However, due to this repeated looping, I decided to terminate the program entirely using 'exit(0);'.

** To indicate where exactly this issue is occurring in the createTweet.c file, I will place an indicating
comment in the createTweet.c file.

This is a known limitation of the current version of my program because it fails to reprompt the user again with the main menu, which prevents them from retrying or selecting another option. If the user wanted to retry or select another menu option, they would need to re-run the program, which is inconvenient.

In the future, I would like to improve this limitation to make my program more user-friendly and easy to use.
