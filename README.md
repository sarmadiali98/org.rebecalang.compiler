# Timed Rebeca to Lingua Franca Compiler

Welcome to the **Timed Rebeca to Lingua Franca Compiler** repository! This tool translates **Timed Rebeca** models into **Lingua Franca (LF)** code. 

The project uses **Spring Framework** and is written in Java. It leverages Maven for dependency management and building. Below are the instructions for installation, usage, and running the program.

---

## Features

1. **Compiles Timed Rebeca Models**: Converts `.rebeca` files into `.lf` files compatible with Lingua Franca.
2. **Batch Compilation**: Processes multiple Rebeca files from a directory and generates corresponding LF files in the output directory.
3. **Customizable Output Path**: Allows users to specify the directory where the compiled LF files are stored.

---

## Project Structure

The project follows a standard Maven structure. Here are key directories and files:

- **Main Code**:
  - `src/main/java/org/rebecalang/compiler/RebecaCompilerMain.java`: The entry point for running the compiler.
  - `src/main/java/org/rebecalang/compiler/modelcompiler/linguafranca/TimedRebecaToLinguaFrancaCompilerFacade.java`: The main logic for handling Timed Rebeca to Lingua Franca translation.
  - `src/main/java/org/rebecalang/compiler/modelcompiler/linguafranca/LinguaFrancaCodeGenerator.java`: The code generator for Lingua Franca.
  
- **Input Models**:
  - `src/test/resources/org/rebecalang/compiler/modelcompiler/models`: Directory containing `.rebeca` files to compile.
  
- **Output LF Code**:
  - `src/test/resources/org/rebecalang/compiler/modelcompiler/compiledLF`: Directory where `.lf` files are generated.

---

## Requirements

- **Java Development Kit (JDK)**: Version 11 or later.
- **Maven**: For building and managing dependencies.
- **Operating System**: Tested on macOS Sequoia 15.1.1, but should work on other systems with JDK and Maven installed.

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://https://github.com/sarmadiali98/org.rebecalang.compiler.git
   cd org.rebecalang.compiler
   ```
2. **Ensure Java and Maven Are Installed: Verify your installations**:

   ```bash
   java -version
   mvn -version
   ```
3. **Install Dependencies: Use Maven to install dependencies**:

   ```bash
   mvn clean install
   ```

---
   
# Running the Compiler

The compiler can process `.rebeca` files in the input directory and generate corresponding `.lf` files.

## Steps to Run

1. **Ensure Models Are in the Input Directory**:  
   Place `.rebeca` files in the following directory:  
   `src/test/resources/org/rebecalang/compiler/modelcompiler/models`

2. **Run the Compiler**:  
   Execute the following Maven command to run the main class:  
   ```bash
   mvn exec:java -Dexec.mainClass="org.rebecalang.compiler.RebecaCompilerMain"
   ```
3. **Check Output**:
   The compiled `.lf` files will be saved in the following directory:
   `src/test/resources/org/rebecalang/compiler/modelcompiler/compiledLF`
