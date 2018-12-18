# ce01 Unix Commands

This exercise is designed to get you acquainted with basic Unix commands.
You will create regular files and directory files and learn how to navigate 
a Unix system from the command line.

## Prerequisite Knowledge

* An introduction to Unix: http://www.ee.surrey.ac.uk/Teaching/Unix/unixintro.html
* Unix Tutorial One, Two, and Three: http://www.ee.surrey.ac.uk/Teaching/Unix
* Installing necessary command line tools to your machine (homebrew for mac, _FIX AND MAYBE USE LINK_

## Creating Directories

By the end of this exericse, you will have a directory hierary similar to the
one seen below. You will use a variety of Unix commands to create this 
heirarchy step-by-step. 

```
exercise1
 |--- README.txt
 |--- photos
 |      |--- 2016
 |      |--- 2017
 |      |--- 2018
 |--- school
 |      |--- 1302
 |            |---notes
 |                  |---day1.txt
 |--- videos
 |      |--- dogs

9 directories, 2 files
```

##Questions
* Give the full Unix command to create the `notes` directory 
(under school/1302) if your present working directory (pwd) is `exercise1`?
* Give the full Unix command to return to your home directory if your pwd 
is `1302`.
* Give the full Unix command to move `day1.txt` from `notes` to `exercise1` 
if your pwd is `exercise1`?
* Give the full Unix command to move `day1.txt` back to `exercise1` from 
`notes` if your pwd is `exercise1`?
* Give the full Unix command to add your group's first and last names to 
the `day1.txt` file (using redirection) if your pwd is the `notes` directory.
* Give the full Unix command to print the contents of `day1.txt` to the 
console if your pwd is the `notes` directory
* Give the command to generate 

## Working with Additional Unix Commands
* Download a book in txt format from https://www.gutenberg.org/.  
Move the text file into your exercise1 directory.
* Write a command to give the number of times the word `the` appears in the 
text.
* Do more with pipes and grep...