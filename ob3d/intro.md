# 0. Introduction

Welcome to another yet unique (as far as I know) programming tutorial.
You'll learn here how to create 3D programs/scenes with the [FreeBasic](https://www.freebasic.net/) programming language and the [OpenB3D library](https://sourceforge.net/projects/minib3d/).

### What is this all about?

Ever wanted to create a 3D game but you were frustrated or even overwhelmed by 3D engines?

Let's face it, 3D programming was never really easy and you'll need a lot of time, practice and experience until you can program something which *actually* looks like something.
OpenB3D tries to be different - it was created with programmers unexperienced in 3D/game programming in mind. That's the reason why you'll barely find any other 3D library as simple as OpenB3D.

The OpenB3D (formerly known as MiniB3D) library ports (almost) all the 3D commands from the not-developed-anymore game programming language [Blitz3D](https://blitzresearch.itch.io/blitz3d) to FreeBasic, which is more modern.

Of course, a simple library like OpenB3D has its downsides - if you want to create the next AAA game, this is the wrong place for you. Due to its age and simplicity, rendered scenes don't have that realistic look we know from modern game engines. And in case you want physics in your game, it's not implemented either. But still, OpenB3D is not only easy and fun to program, you might learn one or two things about 3D/game development. And maybe, FreeBasic + OpenB3D is your steppingstone into the vast world of 3D programming. Sounds interesting? Let's go ahead!

This tutorial series assumes no background in mathematics, computer science or 3D/game development, simple artihmetics and a basic understanding of FreeBasic is all you need (if you don't know FreeBasic, don't worry - there are loads of tutorials/samples on the internet, even in different languages). Everything else will be explained when neccessary.

### What you need

* [FreeBasic](https://www.freebasic.net/), if not already installed
* The [OpenB3D library](https://sourceforge.net/projects/minib3d/)
* An editor of your choice (preferably with FreeBasic syntax highlighting)

### Installation

#### On Windows

Install FreeBasic and download the latest version of OpenB3D (for FreeBasic, Win32). To keep things simple, I suggest creating a working directory somewhere so all your stuff having something to do with OpenB3D is stored in on place. Now extract the files from the OpenB3D archive into your working directory, **nowhere else!** This step is very important if you want your programs to compile/execute.

If you don't want to keep the `.txt` files, you can just delete them. The two important files here are `openb3d.bi` (the header file we include into our programs) and `openb3d.dll` (the actual library which contains the OpenB3D code).

*to do: installation on other systems*

You did all of the steps above? Very well! You are now able to create your first 3D programs!

[Next: Your first OpenB3D program](first.md)