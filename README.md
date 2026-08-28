# Compiler Design Lab (CS4501)

This repository contains the lab experiments for the **Compiler Design** course.

## Experiments

| No. | Experiment | Tools Used |
|-----|-----------|------------|
| 1 | [Lexical Analyzer with Symbol Table](Exp01_Lexical_Analyzer_SymbolTable/) | FLEX |
| 2 | [Lexical Analyzer](Exp02_Lexical_Analyzer/) | FLEX |
| 3 | [Arithmetic Expression Validator](Exp03_Arithmetic_Expression_Validator/) | FLEX + BISON |
| 4 | [Variable Name Validator](Exp04_Variable_Validator/) | FLEX + BISON |
| 5 | [Control Structure Syntax Validator](Exp05_Control_Structure_Validator/) | FLEX + BISON |
| 6 | [Calculator](Exp06_Calculator/) | FLEX + BISON |
| 7 | [Intermediate Code Generator](Exp07_Intermediate_Code_Generator/) | FLEX + BISON |
| 8 | [Type Checker](Exp08_Type_Checker/) | FLEX + BISON |
| 9 | [Code Optimization](Exp09_Code_Optimization/) | FLEX + BISON |
| 10 | [Target Code Generator](Exp10_Target_Code_Generator/) | FLEX + BISON |

## Prerequisites

- **flex** (Fast Lexical Analyzer)
- **bison** (GNU Parser Generator)
- **gcc** (GNU C Compiler)

Install on Ubuntu/Debian:
```bash
sudo apt-get install flex bison gcc
```

## How to Build and Run

Each experiment folder contains its own `README.md` with specific instructions. The general pattern is:

### FLEX-only experiments (Exp 1-2):
```bash
flex <file>.l
gcc lex.yy.c -o <output> -lfl
./<output> <input_file>
```

### FLEX + BISON experiments (Exp 3-10):
```bash
flex <file>.l
bison -d <file>.y
gcc lex.yy.c <file>.tab.c -o <output> -lfl
./<output>
```
