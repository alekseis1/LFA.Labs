# Grammar and Finite Automaton Implementation

This Java project demonstrates the implementation of a grammar and its conversion into a finite automaton.

## Overview

The project consists of two main classes:

1. `Grammar`: Represents context-free grammar and provides methods to generate strings from the grammar.
2. `FiniteAutomaton`: Represents a finite automaton and provides a method to check if a given string belongs to the language described by the automaton.

Additionally, a helper class `Pair` is used to represent pairs of characters in the finite automaton's transition function.

## Usage

1. **Grammar Generation**:
    - Create a `Grammar` object and use the `generateString()` method to generate strings from the grammar.
    - Use the `generateWords()` method to generate multiple strings.
    
2. **Finite Automaton**:
    - Convert the grammar to a finite automaton using the `toFiniteAutomaton()` method.
    - Use the `stringBelongToLanguage(String input)` method of the `FiniteAutomaton` class to check if a given string belongs to the language described by the automaton.

## Running the Code

1. Compile the Java files using a Java compiler:

    ```bash
    javac *.java
    ```

2. Run the main class `Grammar`:

    ```bash
    java Grammar
    ```

## Example

The following is a sample usage of the code:

```java
public static void main(String[] args) {
    Grammar grammar = new Grammar();
    grammar.generateWords();
    System.out.println(grammar.toFiniteAutomaton());

    FiniteAutomaton finiteAutomaton = grammar.toFiniteAutomaton();
    System.out.println(finiteAutomaton.stringBelongToLanguage("abdf")); // Output: true
