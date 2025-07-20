# Brainfuck Fork Bomb Generator

This repository contains a Brainfuck program that prints a classic Bash fork bomb:

```bash
#!/bin/bash
:(){:|:&};:
```

## What is Brainfuck?

Brainfuck is a minimalist esoteric programming language with only 8 commands created in 1993 by Urban Müller. This project demonstrates that even such a simple language can be used to generate dangerous payloads — in this case, a Bash fork bomb.

Despite its simplicity (or because of it), Brainfuck is Turing-complete and can theoretically compute anything that any other programming language can compute.

## About This Implementation

```
+++[>++++++++++>++++++++++>++++++++++<<<-]+++>+++++<[>>++++++++++>++++++++++<<<-]++++>>-<<[>>>++++++++++<<<-]>>>---<<. --. ++++++++++++++.>>+.+++++++.+++++.<<.>>------------.-.++++++++++++++++++.-----------.<<<++++++++++.>>-.<-------.+.>>+++++++++++++++++++.<.>+.<.<---.>>+.<+.-.
```

This program demonstrates some common Brainfuck programming techniques:

- **Using loops for multiplication**: Instead of writing `+` hundreds of times, we use patterns like `+++++++++[>++++++++++<-]` to efficiently build larger numbers
- **Memory management**: Reusing cells and strategically placing values to minimize pointer movement
- **ASCII arithmetic**: Working with ASCII values to generate the specific characters needed


## Running the Code

### Using a Brainfuck Interpreter

```bash
brainfuck forkbomb.bf > evil.sh
chmod +x evil.sh

# (Use caution!) Run the generated script
./evil.sh
```

### Online Interpreters

You can run this code in online Brainfuck interpreters:
- [esolangpark](https://esolangpark.vercel.app/ide/brainfuck)
- [copy.sh/brainfuck](https://copy.sh/brainfuck/)
- [Brainfuck visualizer](https://ashupk.github.io/Brainfuck/brainfuck-visualizer-master/index.html)

## Why Brainfuck?

Programming in Brainfuck is like solving a puzzle. Every simple task becomes a challenge that requires creative thinking. It teaches you to:

- Think about memory management at a low level
- Appreciate the abstractions that modern programming languages provide
- Understand how complex behaviors can emerge from simple rules
- Practice problem decomposition and algorithmic thinking

## Learn More About Brainfuck

- [Brainfuck on Wikipedia](https://en.wikipedia.org/wiki/Brainfuck)
- [Esolangs Wiki - Brainfuck](https://esolangs.org/wiki/Brainfuck)

---

*An exploration of esoteric programming languages and creative problem-solving.*