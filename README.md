# Minishell

A simplified shell implementation in C that recreates basic bash functionality, featuring command parsing, execution, and built-in commands with an Abstract Syntax Tree (AST) approach.



## 🔍 About

Minishell is a 42 School project that challenges students to create a functional shell from scratch. The project focuses on understanding shell mechanics, process management, and command interpretation. This implementation uses an **Abstract Syntax Tree (AST)** for parsing and executing commands, providing a clean and extensible architecture.

**Key Concept**: The shell reads user input, parses it into an AST structure, and executes commands based on the tree traversal, similar to how real shells and compilers work.

## ✨ Features

- **Interactive Shell**: Command prompt with input reading
- **AST-Based Parsing**: Abstract Syntax Tree for command structure representation
- **Command Execution**: System command execution with PATH resolution
- **Built-in Commands**: Essential shell built-ins (cd, echo, pwd, etc.)
- **Pipes**: Command piping with | operator
- **Redirections**: Input/output redirections (<, >, >>)
- **Environment Variables**: Variable expansion and management
- **Quote Handling**: Single and double quote processing
- **Signal Management**: Proper handling of Ctrl+C, Ctrl+D, Ctrl+\
- **Command History**: Basic command history functionality

## 🚀 Installation

1. Clone the repository:
```bash
git clone [your-repo-url]
cd minishell
```

2. Compile the project:
```bash
make
```

3. Run the shell:
```bash
./minishell
```

4. Clean object files (optional):
```bash
make clean    # Remove object files
make fclean   # Remove object files and executable
make re       # Recompile everything
```

## 💻 Usage

### Starting the Shell
```bash
./minishell
minishell$ 
```

### Basic Commands
```bash
# Simple commands
minishell$ ls -la
minishell$ pwd
minishell$ echo "Hello World"

# Built-in commands
minishell$ cd /home/user
minishell$ export PATH="/usr/bin:$PATH"
minishell$ env

# Pipes
minishell$ ls | grep minishell
minishell$ cat file.txt | wc -l

# Redirections
minishell$ echo "test" > output.txt
minishell$ cat < input.txt
minishell$ ls >> log.txt

# Environment variables
minishell$ echo $HOME
minishell$ echo $USER

# Exit the shell
minishell$ exit
```

## 🏗️ Architecture

## 🛠️ Built-in Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `cd` | Change directory | `cd [directory]` |
| `echo` | Display text | `echo [-n] [text]` |
| `pwd` | Print working directory | `pwd` |
| `export` | Set environment variable | `export VAR=value` |
| `unset` | Unset environment variable | `unset VAR` |
| `env` | Display environment | `env` |
| `exit` | Exit the shell | `exit [status]` |

## ⚠️ Error Handling

The shell handles various error conditions gracefully:

- **Syntax Errors**: Invalid command syntax, unmatched quotes
- **Command Errors**: Command not found, permission denied
- **File Errors**: File not found, permission issues for redirections
- **Memory Errors**: Malloc failures, proper cleanup
- **Signal Handling**: Interrupt signals, proper terminal control

## 🧪 Testing

### Test Categories

**Basic Functionality:**
- Simple command execution
- Built-in command functionality
- Environment variable handling

**Parsing Tests:**
- Complex command parsing
- Quote handling (single/double)
- Variable expansion

**Advanced Features:**
- Pipe functionality
- Input/output redirections
- Error handling scenarios

### Example Test Cases

```bash
# Basic commands
echo "Hello World"
ls -la | grep minishell
pwd

# Redirections
echo "test" > file.txt
cat < file.txt
ls >> log.txt

# Environment variables
export TEST_VAR="hello"
echo $TEST_VAR
unset TEST_VAR

# Pipes and complex commands
ls -la | grep minishell | wc -l
cat file.txt | sort | uniq

# Error handling
invalidcommand
cat nonexistent_file.txt
cd /root (permission test)
```

## 🛠️ Technical Skills Demonstrated

- **System Programming**: Advanced understanding of Unix processes and system calls
- **Parser Design**: Implementation of lexical and syntax analysis
- **Data Structures**: Complex tree structures (AST) and memory management
- **Algorithm Design**: Tree traversal algorithms for command execution
- **Process Management**: Fork/exec patterns, pipe management, signal handling
- **C Programming**: Advanced C concepts, pointer manipulation, dynamic allocation
- **Shell Internals**: Deep understanding of how shells work internally
- **Error Handling**: Comprehensive error management across complex systems
- **Memory Management**: Proper allocation/deallocation in tree structures
- **Software Architecture**: Clean separation of parsing, AST, and execution layers

## 📝 Notes

- This project is part of the 42 School curriculum (mandatory part only)
- Developed following 42's strict coding standards (Norminette)
- **Key Innovation**: Uses Abstract Syntax Tree for parsing and execution
- No external libraries except standard C library
- Handles complex command structures through AST representation
- Modular architecture allows for easy extension and maintenance
- Comprehensive memory management for dynamic tree structures

---

**Author**: [Your Name]  
**42 Login**: [Your 42 login]  
**Project**: Minishell (42 Common Core)  
**Date**: [Current Date]

## overview
<img width="868" alt="Capture d’écran 2025-06-12 à 22 21 54" src="https://github.com/user-attachments/assets/8457c8d7-371e-454e-a643-9c8937cb0556" />
