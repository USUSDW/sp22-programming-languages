# Programming Languages Meeting

This repository is for the USUSDW programming language presentations hosted during the Spring 2022 semester. 

*   Presentation 1:
    *   Hosted on February 28th, 2022 
    *   This presentation was on TypeScript and C, presented by Hunter Henrichsen and Dalyn Dalton respectively
*   Presentation 2:
    *   Hosted on March 21st, 2022
    *   This presentation was on Rust and Haskell, presented by Makayden Lofthouse and Jaxton Winder respectively

#### Getting The Sub Repositories
Please do note that some of the work for this presentation exists on other linked Git repositories. After cloning this project, run the commands `git submodule init` and `git submodule update` to clone and update subrepositories that this repository links to.

# Language Presentations
*   C programming language, presented by Dalyn Dalton
    *   [C Presentation Repository](CPresentation)
        *   [Direct Repo Link](https://github.com/USUSDW/sp22-c-presentation)
*   TypeScript programming language, presented by Hunter Henrichsen
    *   [TypeScript Presentation Slides](TypeScript.pdf)
*   Rust programming language, presented by Makayden Lofthouse
    *   [Rust Presentation Repository](Rust)
        *   [Direct Repo Link](https://github.com/USUSDW/sp22-rust-presentation)
*   Haskell programming language, presented by Jaxton Winder
    *   [Haskell Presentation Repository](Haskell)
        *   [Direct Repo Link](https://github.com/USUSDW/sp22-haskell-presentation)

# Language Environment Setup

As we are going to be discussing various programming languages tonight, you may want to prepare your system with an environment that will allow you to try out these programming languages as they are being discussed. We will provide resources dictating how to use these languages locally or in an online environment.

## TypeScript Environments

### Local
Node.js is a JavaScript runtime environment. Node.js contains a TypeScript compiler as part of the various tools installed with Node.js. Node.js is available for all platforms, and an install of Node.js will provide you with all needed tools to use TypeScript.

*   [Node.js download](https://nodejs.org/en/download/)

### Online
The TypeScript official website provides an online playground environment for TypeScript. This is a fully featured environment that will give you all necessary tools to compile and execute simple TypeScript programs.

*   [TypeScript Lang Playground](https://www.typescriptlang.org/play)

Alternatively, there does exist a REPL.it environment for TypeScript which also provides you with all necessary tools to compile and execute simple TypeScript programs.

*   [TypeScript on REPL.it](https://replit.com/languages/typescript)

## C Environments

### Local
To compile C programs locally, we want to get the GNU Compiler Collection, `gcc`. This compiler is available on most OS's and is considered to be one of the "standard" C compilers.

*   [GNU Compiler Collection](https://linuxhint.com/installing_gcc_compiler_ubuntu/)

#### Linux
Install your distributions `build-essentials` or `base-devel` package with your system package manager if you have not already. This package *will* change based on your flavor of Linux used.

*   [Ubuntu](https://linuxhint.com/installing_gcc_compiler_ubuntu/)
*   [Arch](https://wiki.archlinux.org/title/GNU_Compiler_Collection)

#### MacOS
With an installation of the `xcode` development environment, you should have access to the `gcc` and `cc` command line compilers. `gcc` is commonly used, but `cc` is becoming the default C compiler for MacOS.

#### Windows
Just get WSL. Install the Ubuntu distribution of WSL, and follow the instructions for getting `gcc` in Linux with Ubuntu (above). Trust us, it will be *far* easier to learn the basics of C with WSL and `gcc` instead of other Windows proprietary tools. There exists other ways to get a C compiler for Windows, but for our purposes, utilizing WSL and `gcc` within there will be the easiest, most robust, and has a similar workflow to compiling C code on Linux and Mac.

### Online
There exists an online environment for C code on REPL.it. This lightweight environment will emulate an Ubuntu system with the necessary C tools pre-installed. On the left, you are given an editor to the `main.c` file. On the right, you have access to a Bash shell that has `gcc` and easily allows you to compile and test the code you put in `main.c`.

*   [C on REPL.it](https://replit.com/languages/c)

## Rust Environments

### Local
The easiest and recommended way to install Rust is using Rustup. The process is fairly similar for all platforms, and you will be able to get up and running fairly quickly most of the time. The "Getting started" page provides basic info to get Rust installed, and [the book](https://doc.rust-lang.org/book/) has a chapter that has more detailed instructions on installing Rust.

*   [Getting started](https://www.rust-lang.org/learn/get-started)
*   [Chapter on installing Rust](https://doc.rust-lang.org/book/ch01-01-installation.html)

The most important tools that will get installed with Rustup are as follows:

*   `rustup`: tool for managing your Rust installation(s)
*   `rustc`: the Rust compiler
*   `cargo`: Rust's build system which allow you to integrate Rust packages (called "crates") into your project

Most of the time, you will be using `cargo` to build and run your projects, as it is more ergonomic than `rustc`, especially when using external crates. With `rustup`, you can update your Rust toolchains, install nightly toolchains, and install binary crates to use as programs on your system.

### Online
If you want try Rust on the web, you can do so with the Rust Playground or by using REPL.it.

The Rust Playground allows you to switch between stable and nightly toolchains, choosing debug or release optimizations, which edition of the language you want to use, and some development tools such as Rustfmt and Clippy (formatter and linter, respectively).

*   [Rust Playground](https://play.rust-lang.org/)

REPL.it gives you access to a shell, so you can explore the options of `rustc` and `cargo` interactively in that shell (though the project is just a main.rs file rather than a Cargo project, so `cargo` won't be very usable on it).

*   [Rust on REPL.it](https://replit.com/languages/rust)

## Haskell Environments

### Local Tools
The following tools are utilized when compiling and building Haskell projects locally.

#### GHC

Glasgow Haskell Compiler, the most commonly used Haskell compiler, is written in Haskell. It produces some of the fastest compiled Haskell code of all the compilers out there. GHC also has an *interactive REPL*, accessible through `ghci`. Usually, `ghc` is *one of* the tools needed to use Haskell, but it is the most important.

*   **NOTE:** If `ghc` is installed directly and not with Stack, you *may* need to add the `-dynamic` option to `ghc` when compiling on select systems. This is needed to resolve `Could not find module 'Prelude'` error.

*   [Install GHC (NOT RECOMMENDED, USE STACK LISTED BELOW!)](https://www.haskell.org/ghc/)

#### Stack

Stack is a build tool for Haskell code that unifies the work flow of various Haskell tools. It gives you tools to compile (`ghc`) Haskell files, build large projects (`cabal`), and provides easy access to packages on the Hackage package repository; as well as providing a curated subset of "stackage" packages tested for compatability and aimed to promote stability with Haskell packages and avoid dependency issues. If you will be doing any actual project development with Haskell, utilizng Stack is recommended.

An installation of Stack will provide you with *all* necessary tools to compile and build Haskell programs. Installing `stack` will also install a version of `ghc` and `ghci` linked with `stack`.

*   [Install Stack](https://docs.haskellstack.org/en/stable/install_and_upgrade/)

### REPL.it

You can utilize the REPL.it free online Haskell REPL if you would like to follow along with this presentation. In the provided shell, you have immediate access to the `ghci` command to access the interactive Glasgow Haskell Compiler REPL, as well as `ghc` to compile the `main.hs` file you will be editing on the left. Please do note that `stack` *is* installed in this shell, however `stack ghc` and `stack ghci` produce errors. It is recommended to just use `ghc` and `ghci` and avoid `stack` on REPL.it.

*   [Haskell on REPL.it](https://repl.it/languages/haskell)

### Key Shell Commands To Know For Haskell
*   `ghc [FILE]`
    *   Invoke Glasgow Haskell Compiler to compile `[FILE]`
*   `ghci`
    *   Invoke Glasgow Haskell Compiler in interactive mode and get into the REPL
    *   `ghci [FILE]` will load the file and put you into interactive mode
*   `stack`
    *   Interface with the `stack` build tool for Haskell
    *   If `ghc` is installed through `stack` only, it (and `ghci`) can be accessed through `stack ghc`

# Authors, Presenters, and Contributors
A special thanks to everyone who made this presentation possible.

*   Hunter Henrichsen
    *   Author and presenter of TypeScript presentation
*   Dalyn Dalton
    *   Author and presenter of C presentation
*   Jaxton Winder
    *   Author and presenter of Haskell presentation
    *   Authored this repository
*   And you, patrons of the USUSDW!
