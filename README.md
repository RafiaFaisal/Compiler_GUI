

# Parser With GUI: Milestone 1

This project involves implementing the first milestone of a parser in Python along with a GUI for a basic programming language that functions like a calculator.

## Context Free Grammar (CFG)

### Grammar Rules:

- **line →** expression exit_command
- **line →** line expression exit_command
- **line →** exit_command
- **line →** line exit_command
- **line →** UserIn VAR '=' expression exit_command
- **line →** Print expression exit_command

### Expressions:
- **expression →** term
- **expression →** term '+' expression
- **expression →** term '-' expression
- **expression →** term UserIn
- **expression →** VAR

### Terms:
- **term →** factor
- **term →** factor '*' term
- **term →** factor '/' term
- **term →** factor UserIn
- **term →** VAR

### Factors:
- **factor →** primary
- **factor →** primary '^' factor
- **factor →** primary UserIn
- **factor →** VAR

### Primary:
- **primary →** number
- **primary →** '(' expression ')'

### Exit Command:
- **exit_command →** EXIT

## Explanation

### Line:
- An expression followed by an exit command.
- A line followed by an expression and an exit command.
- An exit command.
- A line followed by an exit command.
- User input stored in a variable followed by an expression.
- Print statements take an expression and display the result.

### Expression:
- A term.
- A term followed by '+' and another expression.
- A term followed by '-' and another expression.
- A term followed by user input.
- A variable.

### Term:
- A factor.
- A factor multiplied by another term.
- A factor divided by another term.
- A factor followed by user input.
- A variable.

### Factor:
- A primary expression.
- A primary expression raised to the power of another factor.
- A primary expression followed by user input.
- A variable.

### Primary:
- A number.
- An expression enclosed in parentheses.

### Exit Command:
- The exit command "EXIT" signifies the end of input and triggers the evaluation of the input line.

## Objectives for Milestone 1

- **Implement Grammar Understanding:** Document and clarify the CFG rules to ensure there is a comprehensive understanding before implementation begins.
- **Develop Input Handling:** Create functions or methods to handle input from the user, tokenize this input according to the grammar rules, and manage input errors or invalid syntax effectively.
- **Setup Token Storage:** Implement data structures for storing tokens which facilitate the parsing process in subsequent milestones.

## Next Steps

Upon successful completion of Milestone 1, the project will progress to developing a full parser and integrating a user-friendly GUI to interact with the programming language. The parser will include advanced parsing techniques and error handling capabilities to effectively manage and execute user inputs.

