Introduction
============

This document is an installation guide for *Chisel* (Constructing
Hardware In a Scala Embedded Language) and is intended to prepare your system for subsequent tutorials.  Chisel is a hardware
construction language embedded in the high-level programming language
Scala.

## Development Tool Installation

If you are running Mac or a variant of Linux, you will need to install the appropriate tools for your OS, which are described in the following sections:

### MacOSX

1. Install XCODE, including console tools.

### Linux

Install the following packages:

1. ```g++```
2. ```openjdk-7-jre```

using

``` bash
sudo apt-get install
```

Setting Up the Tutorial
=======================

In subsequent tutorials, you will be using the files distributed in the chisel-tutorial repository. To obtain these tutorials files, ```cd``` to the directory = ```$DIR``` where you want to place the Chisel tutorial and type:

``` bash
cd $DIR
git clone https://github.com/ucb-bar/chisel-tutorial.git
```

Your copy of the Chisel Tutorial repository will then be in ```$DIR/chisel-tutorial```.  Define this as a variable in your bash environment named ```$TUT_DIR```.

This is the Chisel tutorial directory structure you should see, which is explained more in the next tutorial:

``` bash
chisel-tutorial/  
  Makefile
  examples/
    Makefile
    build.sbt
    Accumulator.scala ...
  problems/
    Makefile
    build.sbt
    Counter.scala ...
  solutions/
    Makefile
    build.sbt
    Counter.scala ...
```

The following tutorials will explain features of Chisel by presenting source code examples.  The repository is split into examples, problems, and solutions, where the problems have some piece of the design for you to fill out and where the examples and solutions are meant to be complete designs that should pass the given tests.  In order to run either, you simply need to change directory into the appropriate subdirectory and type ```make``` of the particular lesson name. We will use the repository to first test out if your machine is set up to use Chisel.

To test your Chisel distribution and verify that your system contains all the correct tools, run the following commands:

``` bash
cd $TUT_DIR/examples
make Parity.out
```

This will run a test build and will take a minute before it completes. If your system is set up correctly, you should see a messsage ```[success]``` followed by the total time of the run, and date and time of completion. If you see a success than your system has been set up correctly and you can continute to the next tutorial where we will explain more about the basics of Chisel.

The Tutorials
=============

For these tutorials, we assume basic knowledge of digital circuits and blocks. 
Tutorial 1 will guide you through a quick compilation of the emulator and Verilog generation, and explain some basic constructs such as register and combinational logic.
Tutorial 2 will explain the basics of Chisel.
Tutorial 3 will explain how to use basic primitive types and logical operations that are used in Chisel and how to use them in context of several examples. 
Tutorial 4 will explain how to instantiate components and apply parametrization. 
Tutorial 5 will explain how to use the Chisel test harness. 
Tutorial 6 will explain how to set up your own Chisel project and how to build it.
Tutorial 7 will revisit conditional register updates and explain how to construct memories.
Finally, tutorial 8 will introduce how to use Scala constructs such as ```if...else``` and ```for``` loops.

The following set of tutorials were written using the build settings Scala version 2.10 and Chisel version 2.1.
