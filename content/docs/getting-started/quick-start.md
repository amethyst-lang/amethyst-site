+++
title = "Quick Start"
description = "One page summary of how to install Amethyst."
draft = false
weight = 20
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = "One page summary of how to install Amethyst."
toc = true
top = false
+++

## Requirements

Before using Amethyst, you need to install [nasm](https://nasm.us/index.php), [rust](https://www.rust-lang.org/), and [git](https://git-scm.com/).

## Running the Bootstrap Compiler

```bash
git clone https://github.com/amethyst-lang/amethyst.git
cd amethyst
cargo build --release
```

Alternatively, to install the bootstrap compiler, run the following:
```bash
git clone https://github.com/amethyst-lang/amethyst.git
cargo install --path amethyst
```

## Building the Self Hosted Compiler

This is left empty due to the self hosted compiler being unfinished and unstable.

## Running your First Amethyst Program

## Step 1: Create a new file

Create a file with the following contents and save it as `hello-world.amy`:

```amethyst
(defun main (seqn
    (let msg = "Hello World!\n")
    (syscall 1 1 (cast msg.ptr) msg.len 0 0 0)))
```

## Step 2: Compile

```bash
amethyst ./hello-world.amy
```

## Step 3: Run!

```bash
./a.out
Hello World!
```
