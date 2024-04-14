---
layout: page
title: GSA 08
num: gsa08
nav_order: 10
desc: "Caesar Cipher"
assigned: 2023-02-23 13:00
due: 2023-03-08 23:59
---

# {{page.title}} - {{page.desc}}


## Goals for this assignment

By the time you have completed this assignment, you should be able to

* Process command line arguments
* Work with C-strings
* Iterating arrays
* Read input from `cin`


# Step by Step Instructions

## Step 1: Getting Ready

1. Go to github and find a repo for this assignment assigned to your GitHub id.

2. Log on to your CSIL account.

3. Change into your `~/cs16` directory

4. Clone your empty {{page.num}} repo into your `~/cs16` directory.

5. In your empty repo, do `git checkout -b main` to establish that you are on the `main` branch as your default branch.


## Step 2: Obtain the starter code

The starter code is in this repo:

* <https://github.com/{{site.github_org}}/STARTER-{{page.num}}>

The URL for cloning this repo is this: `git@github.com:{{site.github_org}}/STARTER-{{page.num}}.git`

Previous assignments contain instruction for the process of:
* Adding a `starter` remote for this repo
* Pulling the code from that `starter` remote into your own repo.

Please do those steps now, and then do a `git push origin main` to populate your own repo with the starter code.

If you need help with these steps:
* First consult previous assignments for more detailed instructions.   
* Then, if you are still having trouble, ask the staff for help during discussion section or office hours.

Once you've populated your repo, typing the `ls` command should show you the following files in your current directory

```
$ ls
Makefile	Rectangle.cpp	Rectangle.h	rugfit1.cpp	rugfit2.cpp
$ 
```

## Caesar

Create a file named `caesar.cpp`.  In this file, write a program that implements
a [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher).

Your program should expect  two command line arguments.  The first argument must
be either  `-e` (for encryption) or  `-d` (for decryption).  The second argument
must be a non-negative integer. If the user provides the wrong number of command
line arguments, if the first argument is not expected, or if the second argument
is  not composed entirely of the digits  `0` through `9`,  print a usage message
and exit with exit code 1 to indicate that there was an error:

```
[julius@gallia lab4]$ ./caesar
USAGE: caesar [-ed] [key]
```

If the user provides valid command line arguments,  your program should read its
standard input one line at a time.  It should then either encrypt or decrypt the
line and print the result. When encrypting, all English letters (`a` through `z`
and `A` through `Z`) should be "rotated right" by the user-supplied key  (an `a`
rotated right 3 would become a `d`,  and a `y` rotated right by 3 would become a
`b`).  Capitalization should be preserved,  and all non-letter characters should
be left unchanged.

```
[julius@gallia lab4]$ ./caesar -e 3
abcdefghijklmnopqrstuvwxyz
defghijklmnopqrstuvwxyzabc
Veni, vidi, vici.
Yhql, ylgl, ylfl.
```

When decrypting, all letters should be rotated left.

```
[julius@gallia lab4]$ ./caesar -d 5
Frtw Anshny Trsnf
Amor Vincit Omnia
```

The key may be greater than twenty-six.  Note that when the key is a multiple of
26, the input should be unchanged.

### Tips
To manually send an "end of input" signal while testing, use `Ctrl`+`D` on Linux
and Mac (Ubuntu in WSL counts as Linux),  and use `Ctrl`+`Z` followed by `Enter`
on Windows.


## Step 7: Upload your code to github one last time

Hopefully you remembered to sync your local changes to github often as you were completing the assignment.

If you forgot to do so, be sure to follow the steps in section 1d (above) to upload your final code to github


## Step 8: Submit your code to gradescope

Go to our class site on [www.gradescope.com](www.gradescope.com). Navigate to the assignment for this assignment and submit your code via github.

You should see a score of 100/100 for this assignment.


## Acknowledgement
This GSA is developed from a lab assignment created by Kevin Burk