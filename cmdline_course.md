---
layout: default
---

### KIK-LG219 Command Line Tools for Linguists

Command Line Tools for Linguists provides students who are interested in language technology
a gentle introduction to the UNIX command line environment.
Instead of theoretical knowledge,
the course focuses on getting hands-on experience with working in the command line.
This is intended to make students feel comfortable in operating their own command line.

#### Week 1: Introduction to Command Line Environments

The first week was about setting up your own command line environment.
We were taught some basic commands useful for navigating the command line, and introduced to emacs,
both already familiar to me thanks to previous courses.

After the first week we were able to do the following in the command line:
  * list the contents of our current directory
  * change our current directory
  * download contents from the internet
  * display a text file using less
  * create and remove files and directories
  * copy, rename and move files
  * open and edit a file in text editor

```C
$ cd KIK-LG219/week1/
$ ls
$ touch test.txt
$ emacs test.txt
$ rm test.txt
$ cd ~
```

>Commands: Changing my working directory to the week1 directory, listing the contents of that directory,
creating a text file, opening it in emacs, removing it,
and finally changing the working directory to my home directory.

#### Week 2: Navigating a UNIX System

The first part of the second week saw us learning how to copy, move, and remove directories.
We also learnt more about the UNIX system, its standard system directories and what they contain,
and how the UNIX system protects the privacy of the users with permissions.

The second part dealt with processes and process management.
We learnt how to control processes from the command line, for example,
how to find the PID of a process and kill it, and how to run commands in the background.

In the third part we learnt about working on a remote server using ssh and scp,
how to how to form a remote connection to a server, and how to to copy files to and from a server using scp.

```C
$ chmod a+rwx test.txt
$ mv test.txt sub/
$ mv -r sub/ week2/
```

>Commands: Giving all users persmission to read, write, and execute test.txt, moving the file to sub/,
and moving the directory sub in the directory week2.

#### Week 3: Basic Corpus Processing

The third week we learnt about different character encodings and how to convert between them.
We also learnt about text processing tools in UNIX, some basic commands for them,
how to redirect standard streams, and how to use these commands and redirecting to search text files,
including structured text files. Regular expressions were also introduced.

I had a few problems understanding the material for the week and generating my locale,
but it all worked out in the end.

| code | canonical name | script codes |
| ---- |:--------------:| ------------:|
| aa   | Afar           | Latn         |
| aaa  | Ghotuo         | Latn         |

>Table: An example of what the contents of a structured text file might look like.

```C
$ egrep "^Hello" test.txt | wc -l
$ cat test.txt | tr '\n' ' ' 2> errors.txt
```

>Commands: The first command searches the file test.txt for lines that start with the word "Hello",
then redirects the output to wc, which shows the number of words of the output.
The second command transforms book.txt into one long line and directs potential error messages from tr to errors.txt.

#### Week 4: Advanced Corpus Processing

The fourth week was spent learning more about text processing using UNIX commands.
We chained simple commands into more complex command pipelines,
which allowed us to avoid generating a lot of unnecessary files while operating on text files.

An important part or this week was the sed command which is used to transform text files.
We learnt more about regular expressions since they are instrumental to using sed.

```C
$ cat test.txt | sed 's/cat/dog/' | tr -s '\n\t\r ' '\n' | tr -cd "A-Za-z0-9\n'" | sort | uniq -c | sort -nr
```

>Command: Using sed to replace every instance of the word "cat" in test.txt with the word "dog",
then redirecting to tr to first separate all words into new lines and then remove punctuation,
then piping first to sort, then uniq, then sort again to create a frequency list.

#### Week 5: Scripting and Configuration Files

```
```

>Code:

#### Week 6: Installing and Running Programs

```
```

>Code:

#### Week 7: Version Control

```
```

>Code:


