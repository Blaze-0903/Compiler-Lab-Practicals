# Compiler Construction Lab Assignments 🛠️

This repository contains the practical assignments for the Compiler Construction Laboratory course. These exercises utilize **Lex** (Lexical Analyzer Generator) and **Yacc/Bison** (Parser Generator) to implement various components of a compiler.

---

## Student Details

* [cite_start]**Name:** Sujal Junghare [cite: 4]
* [cite_start]**PRN:** 22070521089 [cite: 5]
* [cite_start]**Department:** CSE [cite: 7]
* [cite_start]**Division:** C [cite: 6]
* [cite_start]**Semester:** VII [cite: 8]
* [cite_start]**Course Code:** T7478 [cite: 9]
* [cite_start]**Course Name:** Compiler Construction Lab [cite: 3]

---

## Assignments List

The following is a list of the practical assignments completed for the course:

### 1. Number to Digit Conversion (Lex)
* **Objective:** To recognize the English word representation of digits (zero through nine, in both lowercase and uppercase) and print their corresponding numerical digit.
* **Example Input/Output:** `one` $\to$ `1`, `ZERO` $\to$ `0`

### 2. File Statistics Counter (Lex)
* [cite_start]**Objective:** To count the number of lines, spaces, tabs, words, and characters from an input sentence or file. [cite: 11]

### 3. Word Counter Starting with 'A' (Lex)
* [cite_start]**Objective:** To count the total number of words in the input text that start with the letter 'A' or 'a'. [cite: 12]

### 4. Case Conversion (Lex)
* [cite_start]**Objective:** To convert all **lowercase** letters in the input to **uppercase** and all **uppercase** letters to **lowercase** using ASCII value manipulation. [cite: 13]

### 5. Decimal to Hexadecimal Conversion (Lex)
* [cite_start]**Objective:** To recognize decimal numbers from the input and convert them into their equivalent hexadecimal representation. [cite: 14]

### 6. Line Ending Test (Lex)
* [cite_start]**Objective:** To test if an input line ends with the specific string `com` (e.g., in an email address or URL). [cite: 15]

### 7. Postfix Expression Evaluation (Lex & Yacc)
* [cite_start]**Objective:** To implement a basic calculator capable of evaluating **postfix expressions** using Lex for tokenization and Yacc for parsing and evaluation. [cite: 16]

### 8. Simple Desk Calculator with Error Recovery (Lex & Yacc)
* [cite_start]**Objective:** To create a functional desk calculator that handles arithmetic expressions with operators (`+`, `-`, `*`, `/`) and includes error recovery mechanisms for invalid syntax. [cite: 17]

### 9. Parser for FOR Loop (Lex & Yacc)
* [cite_start]**Objective:** To implement a parser that checks the syntax and validates the structure of a simplified **FOR loop** statement. [cite: 18]

### 10. Intermediate Code (IC) Generator (Lex & Yacc)
* [cite_start]**Objective:** To implement a simple intermediate code generator (using Three-Address Code) for basic arithmetic expressions, demonstrating the intermediate phase of compilation. [cite: 19]

---

## Compilation and Execution

The general workflow for compiling and running these assignments involves the following steps in a Unix-like environment:

1.  **Generate Lexer (C code):**
    ```bash
    lex <filename>.l 
    ```
2.  **Generate Parser (C code and Header for Yacc assignments):**
    ```bash
    yacc -d <filename>.y # Use only for Yacc/Bison files (e.g., practical7_1089.y)
    ```
3.  **Compile the generated C code:**
    ```bash
    # For Lex-only files
    cc lex.yy.c -ll -o <output_name>
    # For Lex & Yacc files
    gcc lex.yy.c y.tab.c -ll -o <output_name> 
    ```
4.  **Execute the program:**
    ```bash
    ./<output_name>
    ```

**Note:** The output file names in the document (e.g., `a.out`, `postfix`, `calc`, `prac9`, `prac10`) vary depending on the practical.
