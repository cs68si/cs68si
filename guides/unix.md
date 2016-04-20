---
layout: page
title: Guide to the unix command line
---

*Prepared by Alexandre Becker, cs107 TA, Modified for CS68SI by Kai Marshland*

## Unix commands

This tutorial walks you through the use of most basic unix commands for navigating the file system, viewing files, and reading the manual pages.

### Browsing the file system

Open a terminal. The terminal window will show:

    %

What does this mean? The `%` is called the "command prompt".
(Depending on what flavor of unix and your login profile,
you may see a different prompt.)

Let's try running our first command. 
Enter the `ls` command and then press the return key (or "enter" key):

    % ls
    Documents  Downloads   Mail

What does this command do? It lists all the files and folders contained in the current directory. To include more details about each file, such as the type or the size, you can add the `-l` flag to the command:

    % ls -l

Then, you may need to change the current directory. Use the `cd` command to set a different directory as current:

    % cd Documents

Typing `cd` by itself, returns you to your home directory (the root
of your personal file system).
Wherever you are in the filesystem, 
you can print the full path of the current directory with the `pwd` command.

    % cd
    % pwd
    /Users/hanrahan
    
Congratulations, you can now browse and display the files 
wherever you have access on your machine!

### Creating folders and files

You may want to create a folder dedicated to cs107. 
To do that, go in the folder where you want to create a directory,
and use the `mkdir` command:

    % mkdir Class
    % cd Class
    % ls
    Class
    % mkdir cs107
    % ls
    cs107

You can create a new file 'foo.c' using your favorite editor (Emacs or Vim). 

You can move the file to another directory with the `mv source destdir` command.

    % mv foo.c cs107

If destination is a file, the `mv source destination` command will rename the file:

    % cd cs107
    % ls
    foo.c
    % mv foo.c bar.c
    % ls
    bar.c

You can also use the `cp source destination` command to make a copy of the file with a new name.

    % cp bar.c foo.c
    % ls
    bar.c foo.c

To delete folders and fies, use these commands:

+ `rm file` will delete a file
+ `rmdir folder` will delete a folder, if it is empty
+ `rm -r folder` will delete a folder and all the files or subdirectories that it contains

### Viewing a file

Besides opening a file your favorite text editor (e.g. Emacs or Vim), 
you can view its contents with `cat file` or `more file`. 
Whereas  `cat` will print the entire file in one go,
`more` allows you to scroll up and down.
You can use these keystrokes to scroll:

+ __space__ to scroll down
+ __b__ to scroll up (b stands for "backward")
+ __q__ to quit
+ __/__ to open a search box at the bottom of the screen. After typing the word that you are looking for, its occurrences will be highlighted. Use __n__ and __p__ to jump to the next and previous occurrence of the word.

### Using the man pages

Each command has a manual page that shows you how to use it 
and what its options are.
You can view a man page using `man command`.
This is one of the most useful commands to know!

    % man ls

Tip: you can use the same keyboard shortcuts to scroll the man page as in the `more` program!

Most commands also accept options to print out a short *usage* reminder.
For example,

    % more --help

list all the options and keyboard shortcuts. 
If `--help` doesn't work, try `-h`.


Philip Guo, a former PhD student at Stanford has also produced some nice
[videos](http://pgbovine.net/command-line-tutorial.htm) that introduce basic
unix commands.

