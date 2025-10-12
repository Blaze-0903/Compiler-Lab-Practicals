# Compiler Construction Lab Assignments 🛠️

This repository contains the practical assignments for the **Compiler Construction Laboratory** course. These exercises primarily focus on implementing components of a compiler using **Lex** (Lexical Analyzer Generator) and **Yacc/Bison** (Parser Generator).

---

## Student Details

* **Name:** Sujal Junghare
* **PRN:** 22070521089
* **Department:** CSE
* **Division:** C
* **Semester:** VII
* **Course Code:** T7478
* **Course Name:** Compiler Construction Lab

---

## Assignments List

Below is a summary of the practical assignments completed:

### 1. Lexical Analyzer for Word-to-Digit Conversion
* **Objective:** To recognize the English word representation of digits (e.g., "one", "ONE", "zero", "ZERO") and print their corresponding numerical digit (e.g., 1, 0).

### 2. Input File Statistics Counter
* **Objective:** To count various statistics from an input file or text, including the number of **lines**, **spaces**, **tabs**, **words**, and total **characters**.

### 3. Word Counter Starting with 'A'
* **Objective:** To count the total number of words in the input text that begin with the letter 'A' or 'a'.

### 4. Case Conversion
* **Objective:** To implement a program that converts all **lowercase** characters to **uppercase** and all **uppercase** characters to **lowercase**.

### 5. Decimal to Hexadecimal Conversion
* **Objective:** To read decimal numbers from the input and convert them into their equivalent **hexadecimal** format (e.g., $935 \to 0\text{x}3\text{A}7$).

### 6. Line Ending Tester
* **Objective:** To test and print lines from the input that end with the specific string `"com"`.

### 7. Postfix Expression Evaluation (Lex & Yacc)
* **Objective:** To implement a parser for evaluating **postfix arithmetic expressions** (Reverse Polish Notation).

### 8. Simple Desk Calculator with Error Recovery (Lex & Yacc)
* **Objective:** To build a fully functional desk calculator that handles basic arithmetic operations ($+$, $-$, $*$, $/$), parentheses, and includes an **error recovery** mechanism.

### 9. Parser for FOR Loop (Lex & Yacc)
* **Objective:** To create a parser that analyzes and validates the basic syntax structure of a **FOR loop** statement.

### 10. Intermediate Code (IC) Generator (Lex & Yacc)
* **Objective:** To implement a program that generates **Three-Address Code (TAC)** as an intermediate representation for arithmetic expressions, following the order of precedence. (e.g., $a + b / c * d \to t1 = b / c; t2 = t1 * d; t3 = a + t2$)

---

## Compilation and Execution Guide

The general procedure for compiling and executing these Lex and Yacc programs on a Unix-like system (like Linux) is as follows:

| Step | Command for Lex-Only Files | Command for Lex & Yacc Files | Description |
| :--- | :--- | :--- | :--- |
| **1. Lex** | `lex <filename>.l` | `lex <filename>.l` | Generates the lexical analyzer C file (`lex.yy.c`). |
| **2. Yacc** | N/A | `yacc -d <filename>.y` | Generates the parser C file (`y.tab.c`) and token header (`y.tab.h`). |
| **3. Compile** | `cc lex.yy.c -ll -o <output>` | `gcc lex.yy.c y.tab.c -ll -o <output>` | Compiles the generated C files and links the Lex library (`-ll`). |
| **4. Execute** | `./<output>` | `./<output>` | Runs the compiled executable. |

**Example Compilation (for Postfix Evaluator):**
```bash
yacc -d postfix_1089.y
lex postfix_1089.l
gcc lex.yy.c y.tab.c -o postfix -ll
./postfix
