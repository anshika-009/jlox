# jlox - Java Tree-Walk Interpreter

A custom tree-walk interpreter for the **Lox** programming language, implemented in Java based on Robert Nystrom's acclaimed book, [*Crafting Interpreters*](https://craftinginterpreters.com/).

## 📌 Overview

`jlox` processes Lox source code through standard compiler stages: tokenizing the input source, parsing token streams into an Abstract Syntax Tree (AST), printing expression structures, and executing program logic via file input or an interactive REPL.

## 🗂️ Project Structure

```text
src/main/java/org/example/
├── AstPrinter.java   # AST traversal and pretty-printing utility
├── Expr.java         # Abstract Syntax Tree expression node definitions
├── Lox.java          # Main driver, file reader, error reporter, and REPL runner
├── Parser.java       # Syntax analyzer and recursive descent parser
├── Scanner.java      # Lexical analyzer / Tokenizer
├── Token.java        # Token representation data structure
└── TokenType.java    # Enum definitions for language tokens

🚀 Features

    Lexical Analysis: Scans source code and converts characters into structured tokens.

    Syntactic Analysis: Uses recursive descent parsing to construct expression syntax trees.

    AST Visualization: Outputs formatted string representations of syntax trees using AstPrinter.

    Flexible Execution: Supports running .lox script files or executing commands interactively via a command-line REPL.

    Error Handling: Centralized reporting for lexical and syntax errors with precise line tracking.

🛠️ Getting Started & Usage
Prerequisites

    Java Development Kit (JDK): Version 8 or higher

    Git

1. Compile the Source Files

Navigate to the root directory and compile the Java source files into a target bin folder:
Bash

javac -d bin src/main/java/org/example/*.java

2. Run the Interpreter

    Interactive REPL Mode:
    Bash

    java -cp bin org.example.Lox

    (Once running, type expressions at the >  prompt)

    Execute a Lox Script File:
    Bash

    java -cp bin org.example.Lox path/to/your/script.lox
