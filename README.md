# ce01 Unix Commands

![Approved for: Fall 2020](https://img.shields.io/badge/Approved%20for-Fall%202020-blueviolet)

This exercise is designed to get you acquainted with basic Unix commands.
You will create regular files and directory files and learn how to navigate 
a Unix system from the command line.

## Prerequisite Knowledge

* [An introduction to Unix](http://www.ee.surrey.ac.uk/Teaching/Unix/unixintro.html)
* [Unix Tutorial One, Two, Three, and Four](http://www.ee.surrey.ac.uk/Teaching/Unix)

## Course-Specific Learning Outcomes

* **LO1.a:** Navigate and modify files, directories, and permissions in a multi-user Unix-like environment.
* **LO1.b:** (Partial) Execute, redirect, pipe, and manage programs/processes in a multi-user Unix-like environment.

## Before You Begin

If you haven't done so already, you should complete one of the setup instructions provided below before you begin.

* [MacOS Setup Instructions](https://github.com/cs1302uga/cs1302-exercises/blob/master/misc/MacOS.md)
* [Windows 10 Setup Instructions](https://github.com/cs1302uga/cs1302-exercises/blob/master/misc/Windows10.md)

If you have access to your Odin account, then you may login and perform the exercise there.
Otherwise, you may perform the exercise on your local machine. Instructions for logging into
Odin can be found here: [Odin Setup](https://github.com/cs1302uga/cs1302-exercises/blob/master/misc/OdinSetup.md)

## Creating Directories

By the end of this exercise, you will have a directory hierarchy similar to 
the one seen below. You will use a variety of Unix commands to create this 
heirarchy step-by-step. **NOTE: you should not create this hierarchy before moving on.** We provide the heirarchy
here so you can reference it as you work and to show where we are headed.

```
exercise1
 |--- SUBMISSION.md
 |--- photos
 |      |--- 2017
 |      |--- 2018
 |      |--- 2019
 |--- school
 |      |--- 1302
 |            |---notes
 |                  |---day1.txt
 |                  |---names.txt
 |--- lit_works
 |      |--- 1661-0.txt

8 directories, 4 files
```

## Questions

In your notes, clearly answer the following questions. These instructions assume that you have setup
your local machine following the instructions linked to on eLC and the syllabus.

**NOTE:** For each step, please provide in your notes the full command that you typed to make the related 
action happen along with an explanation of why that command worked. Some commands require multiple options. 
It is important to not only recall what you typed but also why you typed each of them. If done properly, your 
class notes will serve as a helpful study guide for the exam. 

## Exercise Steps

### Checkpoint 1 Steps

1. Carefully read the following:

   > If at any point while working through this exercise, you encounter an error message, don't worry. Carefully 
   > read and process the error message to see what went wrong. In some cases, the error messages are expected
   > and we want you to use them as a hint. If, however, the error message doesn't make sense or you 
   > can't figure out how to proceed, your instructor or a TA will be glad to help out.

1. When you launch your terminal emulator, what is the absolute path of the directory it places you 
   in? What command can you use to figure it out?

1. What series of commands can be used to create the `exercise1`, `photos`, and yearly 
   subdirectories under `photos` in the example provided above? No need to create `school` or `lit_works`
   at this time. Assume that you change into each directory, as needed, after making it. Write all commands
   used in your notes.

1. Change into the `2019` directory. From within `2019`, what single command can be used to change into the `photos`
   directory? Go ahead and execute the command to navigate to `photos`.
 
1. Change into the `2019` directory. From within `2019`, what single command can be used to change into the `exercise1`
   directory? Go ahead and execute the command to navigate to `exercise1`.

1. Your present working directory (pwd) should be `exercise1`. From this directory, without changing into other
   directories (your answer should not use `cd`), what series of commands can be used to create the `school`, 
   `1302`, and `notes` directories? 

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-1-success?style=for-the-badge)

<hr/>

### Checkpoint 2 Steps

1. Your present working directory (pwd) should be `exercise1`. What series of commands can be used to
   verify that the directories in the previous question were successfully created? Assume that
   you never change directories for this question.

1. If you are elsewhere, change into the `exercise1` directory. Use the `rmdir` command to remove (delete)
   the `school`, `1302`, and `notes` directories. Write and describe all commands used in your notes.
   
1. If you are elsewhere, change into the `exercise1` directory. Attempt to recreate the directories you
   just removed with the single command `mkdir school/1302/notes`. Note the error message received. It is
   possible to create all three directories with a single command. Use the `man` command
   to learn more about the `mkdir` options that are available and determine which option needs to
   be placed between `mkdir` and `school/1302/notes` to make this work. Execute the modified command
   and verify that all three directories have been created.

1. The `echo` command is a pretty popular Unix command. What command can be used to learn more
   about it?

1. Change into the `notes` directory. Use `echo` and output redirection to add the first and last name
   of one group member (or just your name if you are not working in a group) to a regular file called 
   `day.txt` in the present working directory. Verify that the file contains the desired text **without 
   using a text editor**. Note the command(s) used.

1. Use `echo` and output redirection to add the first and last name of a different group member to 
   `day.txt` without overwriting the first group member's name. Verify that the file now contains 
   **both** names. If only the one name appears, repeat the last step and try again. Once the contents
   of the file are correct, note the command(s) used with an explanation of why those commands worked.

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-2-success?style=for-the-badge)

<hr/>

### Checkpoint 3 Steps

1. If you are elsewhere, change into the `notes` directory. Rename `day.txt` to `day1.txt`. Write the
   command you used in your notes.
   
1. Change into the `exercise1` directory. Without changing directories again, copy `day1.txt` to `names.txt`.
   Both files should now be contained in the `notes` directory.

1. Assume you are still in the `exercise1` directory. What command(s) can be used to verify that
   you actually copied the file in the previous question to the desired location?

1. Change to the `1302` directory. Without changing directories again, copy the entire contents of the 
   `notes` directory into the `exercise1` directory. Write the command you used in your notes. Verify
   that the two text files now exist in both locations.

1. Assume you are still in the `1302` directory. What single command can be used to delete both text 
   files located in the `exercise1` directory? Execute the command to delete both text files from `exercise1`.
   They should now be located in the `notes` directory only.

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-3-success?style=for-the-badge)

<hr/>

### Checkpoint 4 Steps

1. Change to the `exercise1` directory, create the `lit_works` subdirectory, and change your present
   working diretory to `lit_works`.

1. In your web browser of choice, visit
   [Project Gutenberg](https://www.gutenberg.org/) and find the `Plain Text UTF-8` version of the 
   _Adventures of Sherlock Holmes_ by Sir Arthur Conan Doyle. Use the `wget` command to download 
   this file into the `lit_works` directory. How many lines, words, and bytes are in this file?

1. As you might suspect, the name "Sherlock" (case sensitive) appears on many lines in this file. 
   What command can be used to display only these lines to standard output? 

1. What single command can be used to output the number of lines containing the name "Sherlock" 
   (case sensitive)? Hint: Your answer may need to use pipes.

1. Consider your response to the previous two questions. What commands can be used to output
   the number of lines containing both the word "Sherlock" (case sensitive) and "Watson"
   (case sensitive)? Hint: Your answer may need to use pipes.

1. What command can be used to count the number of lines in this file that
   contain the name "Sherlock" with any capitalization (case insensitive)?
   Hint: you may want to look at options in the `man` pages for a 
   hint.
   
1. **[TRICKY]** What command can be used to count the number of lines in this file that
   contain the name "Sherlock" with any capitalization other than "Sherlock"? For example, 
   "sHerlock", "sherlock", "sherLOCK", etc. are examples of capitalizations that are not
   literally "Sherlock". Hint: you may need to look up additional options in the `man`
   pages.

<hr/>

![CP](https://img.shields.io/badge/Just%20Finished%20Checkpoint-4-success?style=for-the-badge)

<hr/>

### Submission Steps

**Each student needs to individually submit their own work.**

1. Create a plain text file called `SUBMISSION.md` directly inside the `exercise1`
   directory with the following information:

   1. Your name and UGA ID number;
   1. Collaborator names, if any; and
   1. The answers to the questions in steps 2 - 7 in Checkpoint 4.
   
   Here is an example of the contents of `SUBMISSION.md`. You would need to write actual answers for Q2-Q7:
   
   ```
   1. Sally Smith (811-000-999)
   2. Collaborators: Joe Allen, Stacie Mack
   3. Q2: ...
      Q3: ...
      Q4: ...
      Q5: ...
      Q6: ...
      Q7: ...
   ```

1. Change into the parent directory of `exercise1` and use the `submit` command to submit this exercise to `csci-1302`:
   
   ```
   $ submit exercise1 csci-1302
   ```
   
   Read the output of the submit command very carefully. If there is an error while submitting, then it will displayed 
   in that output. Additionally, if successful, the submit command creates a new receipt file in the directory you 
   submitted. The receipt file begins with rec and contains a detailed list of all files that were successfully submitted. 
   Look through the contents of the rec file and always remember to keep that file in case there is an issue with your submission.

   **Note:** You must be on Odin to submit.
     
<hr/>

![CP](https://img.shields.io/badge/Just%20Finished-Submission-success?style=for-the-badge)

<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>

