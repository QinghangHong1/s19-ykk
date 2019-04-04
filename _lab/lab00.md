---
layout: lab
num: lab00
ready: true
desc: "Getting started"
assigned: 2019-04-03 8:00:00.00-7
due: 2019-04-09 23:00:00.00-7
---

# Introduction

This lab is an introduction to programming on CSIL and the tools you'll need for this course. The intended outcome is:

* Learn about the tools you will be using in this class (Gradescope and github).
* Create the necessary accounts.

This lab must be completed **INDIVIDUALLY**. 

***

# Setup the tools for this course

As you are working through the lab, we recommend reading the entire section with all of its steps before trying it out yourself. Doing so will help you see the bigger picture of how the steps fit together. 

## Create a CoE account 

We encourage you to complete all programming assignments by logging in to the machines in the Computer Science labs, or to connect remotely. To do this you will need a **College of Engineering account**. If you don't have one already, you can create an account online at <a href="https://accounts.engr.ucsb.edu/create" target="_blank">https://accounts.engr.ucsb.edu/create</a>.

If you are enrolled in <i>any</i> CoE course this quarter (including CS16), you can create your account immediately. Otherwise, you need to contact the ECI Help Desk at help@engineering.ucsb.edu.

## Setup GitHub and add yourself to our organization

We have created an organization called `ucsb-cs16-s19-ykk` on github.com where you can create *private* repositories (repos) for your assignments in this course. The advantage of creating private repos under this organization is that the course staff (your instructors and TAs) will be able to see your code and provide you with help, without you having to do anything special.

To join this organization, you need to do three things.

1. If you don't already have a github.com account, create one on the "free" plan. Visit [https://github.com/](https://github.com/) and use your **@umail.ucsb.edu** address to create an account (you shouldn't use any other address, since the system won't allow you to log-in).

2. If you don't already have your **@umail.ucsb.edu** email address associated with your github.com account, go to "Settings", add that email, and confirm that email address (using the confirmation link that was sent to the email address you initially provided).

3. Visit our Github Sign Up Tool at [https://ucsb-cs-github-linker.herokuapp.com/](https://ucsb-cs-github-linker.herokuapp.com/), login with your github.com account, click "Home", find this course (CS16-S19-ykk), and click the "Join course button". Doing so will automatically send you an invitation to join the course organization on github (see next step).

4. You can go straight to <https://github.com/ucsb-cs16-s19-ykk> and see the invitation there (if you're logged in). Accept the invitation that appears in your browser (from step 3) or log into your account on [https://github.com/](https://github.com/) to accept the invitation.

## Setup Gradescope

We will use Gradescope to grade all your quizzes, homeworks, exams, and lab/programming assignments. I have added everyone (using your **@umail.ucsb.edu** accounts) who is currently enrolled in the course to the Gradescope system. You should have received an email notification with instructions about logging into [Gradescope](https://gradescope.com/login). Once you follow the instructions to set your password, you should have access to our course on Gradescope. 

The lab assignment "Lab00" should appear in your Gradescope dashboard for your CS 16 course. You will need to submit your code for Lab00 there.

***

# Implement and submit a simple C++ program 

## Step 1: Open a Terminal and write a "Hello World" program 

The first step in every assignment will be to open a <b>terminal window</b>, which will be the environment you use to write, compile, and run your programs.

* If you are working on a machine in the Phelps 3525
    please see [Step 2a](#step2a){: data-ajax="false"} for further instructions.

* If you are working on a machine in the Computer Science Instruction Lab (CSIL), you'll be working on one of the following machines: `csil-01.cs.ucsb.edu`, `csil-02.cs.ucsb.edu`, etc.(though `csil-48.cs.ucsb.edu`). Please see [Step 2a](#step2a){: data-ajax="false"} for further instructions.

If you are working on your laptop, whether Windows, Mac or Linux, the instructions [here](#) will tell you how to connect to `csil-[01-48].cs.ucsb.edu`. 
**For this lab, you should be using the lab computers.**


## Step 2: Connecting to CSIL

### Step 2a: Opening a Terminal on a Phelps or CSIL Lab Machine <a name="step2a"></a>

1. Log in to the machine using your CoE account credentials (i.e., your username and password that you created using instructions above).

2. Find the <i>Activities</i> menu, which is in the top-left corner of the screen. Click on it to open the menu.

3. Next, type "shell" in the search box. Then click the "Terminal" application which appears.

4. You should now see a terminal window open. You can open more tabs or windows from the Terminal application's menu. **Skip to Step 3** and read the other Step 2 steps later when you attempt to log in remotely.

<br />


## Step 3: Create cs16 and lab00 directories<a name="step3"></a>

Now that your environment is set up, you will need to create a directory (a folder is also called a <i>directory</i> in Linux) that will contain all your work for the course. Then, inside that directory, you will need to create another directory to contain your work for this assignment.

To create your CS16 directory, use the `mkdir` command. Type the following in the terminal and press Enter:

```
$ mkdir cs16
```

The <b>$</b> represents the terminal prompt; <i>you won't type this character</i>. Whenever you see it, that means that the following command is intended to be typed into the terminal window and run by pressing Enter.

You can see list of files and directories in the current directory with `ls` command. Type the following in the terminal and press Enter:

```
$ ls
```

You should be able to see the directory you just created i.e., **cs16**.

Now move into that new CS16 directory with the `cd` command as follows:

```
$ cd cs16
```

Now create and move into a **lab00** directory:

```
$ mkdir lab00
$ cd lab00   
```

Note that you could have alternatively created the entire path by adding the flag `-p` to the `mkdir` command (i.e., `make -p cs16/lab00`).

At any time, you can check what directory you are current in with the command `pwd`. It will output the full path of the current directory. For example, if you are inside your <b>lab00</b> directory, you might see:

```
/cs/student/yourcsilname/cs16/lab00
```

Knowing how to navigate a UNIX environment and issue UNIX commands is VERY valuable to computer scientists and engineers. To learn more UNIX commands, there are lot of cool Web resources and books on the topic. This is one website with a good introductory page: [Useful unix commands](http://mally.stanford.edu/~sr/computing/basic-unix.html).

## Step 4: Edit text files <a name="step4"></a>

Let's take a little detour on how to best create and modify text files. These will carry all the code (regardless of computer language) that we want to assemble, compile, and execute.

You are surely all familiar with Microsoft Word as a widely-used "word processor", but please DO <b>NOT</b> USE MS WORD TO WRITE PROGRAMS!!! :)<br>
Instead, for programming, you have access to a very large number of excellent text editors - most of them are free to use! All software developers have their preferences, but learning the basics of a Unix-based command line text editor is very important. Every student who intends to study computer science should learn a popular Unix-based text editor (vim or emacs), since it is not uncommon that the machine you need to work on does not have a Graphical User Interface (GUI), and you may be forced to use a command-line editor (this is especially true when connecting remotely). The two most popular Unix-based command line editors are <b>vim</b> and <b>emacs</b>. 

In fact, <i>AND PLEASE NOTE THIS</i>, no one editor is necessarily "better" than another. It is a matter of your preference. For the first couple labs in this class, we will be using <b>vim</b> to work on our programs.

## <b>vim</b> for UNIX-based OS

vim (or sometimes called vi) is a popular editor that's also available on just about every UNIX machine (including the ones that you're using in the CS labs) and UNIX-based machines (like MacOS computers).

To customize your vim environment for a better coding experience with C/C++, let's add the following lines to a  **.vimrc** file in your home folder (**make sure to use this exact filename, since it is a system file**, there are no spaces in `~/.vimrc`).

Let's dive in! Open the file: 
```
$ vim ~/.vimrc
```

Look at the bottom of the vim window to check if you are in the "Insert" mode (if you are not, then type `i`). Either copy/paste (by right-clicking using the mouse, if you are using the terminals in the lab) or type the following four lines into the file:

```
set nu
syntax on
set autoindent
set cindent
```

Exit the "Insert" mode by pressing Esc key on the keyboard, then type `:wq` to write and quit the file (the colon <b>`:`</b> is important! Don't leave it out!). 
**Make sure that you exit out of that file**: the rest of the lab will have you create **new** files.


Again, to learn how to use vim, there is no substitute for **practice**!!! Here are some more [vim hints](vim_hints/) to refer to. We don't expect you to be experts in vim this quarter, but you should definitely pick up "survival" skills. A little later this quarter, we will confirm that you know how to do the "basic eight" ([vim: basic eight](https://ucsb-cs16.github.io/topics/vim_basic_eight/)). 

There are multiple online resources that you can look at and here are some of them:
* <a href="http://www.vim.org/about.php" target="_blank">About vim</a>
* <a href="https://www.engadget.com/2012/07/10/vim-how-to/" target="_blank">Vim: How to</a>
* <a href="http://tnerual.eriogerg.free.fr/vimqrc.html" target="_blank">vim commands - a handy reference card</a>
* <a href="https://www.fprintf.net/vimCheatSheet.html" target="_blank">another reference cheat sheet for vim</a>
* we posted a printable cheat-sheet of Vim commands on Piazza

## Step 5: Create and edit a file containing a C++ program <a name="step5"></a>


This assignment only needs you to write a program that prints out two lines on the display, and nothing else. <b>The output should look EXACTLY as follows</b> (*no space before or after each line, except the 2 newlines*):

```
Hello, world!
I am ready for CS16!
```

Start with a "skeleton program" (or template) that contains the necessary structure but that does not do anything:

```cpp
#include <iostream>

using namespace std;

int main() {
    // Your printing code should go here

    return 0;
}
```
Go ahead and type this in to the **new file** called **hello.cpp** (you will need to do **`vim hello.cpp`**). Alternatively, you can copy and paste it directly from this page.

**Important note**: For students familiar with Python, remember that lines starting with the <b>`#`</b> character are not comments in C++. Rather, they are important `include` lines that allow your program to use the input and output functionality. Make sure to copy those lines in your program as well. Only <b>`//`</b> or <b>`/*`</b> create comments in C++.

Next, you will need to replace the comment with code to print out the expected output. Comments in C++ are lines that start with <b>`//`</b> or text between <b>`/*`</b> and <b>`*/`</b>. The latter style of comment allows text to span multiple lines.


To print out text to the terminal, you can use the <b>`cout`</b> stream. To output something use the <b>&lt;&lt;</b> operator as shown below:

```
cout << "This will be printed out to the terminal" << endl;
```

**Note**: `endl` ends with a letter "el" (l), **not** a number "one" (1)!
The `endl` command will cause a newline (i.e. a carriage return) to be printed and the next print will go on the next line.

You can adapt this line to achieve the objective of the assignment. <b>Remember that we need to print two lines, each with a newline at the end.</b> You can do this with one or two statements.

## Step 6: Compile the Code <a name="step6"></a>

Now that the code is written, we need to <em>compile</em> it. This will be done using a special program called a <em>compiler</em>.

Before moving on, <b>make sure you save your code</b> and close the text editor. The following step will be done in the terminal.

For C++ code we will use the <b>`g++`</b> compiler that's built into many UNIX machines (it even works on most MacOS terminal programs). You can compile the <b>hello.cpp</b> file into an executable called <b>hello</b> with the following command:

	$ g++ -o hello hello.cpp

This will compile your code and make an executable version of it. Specifically, it will tell the compiler to take the source code file <b>hello.cpp</b> and compile and link it to an executable called <b>hello</b>.

If the compilation is successful, you won't see any output from the compiler, but if you issue a UNIX `ls` command, you should see a new file has appeared: one called <b>hello</b>. You can then use the following command to run your program:

	$ ./hello

Which means "in the current directory, as represented by the <b>.</b> character, run the program <b>hello</b>". You should then see the program output the two expected lines.

The other possibility is that the program may <b>not compile successfully</b>. What to do then?<br>
If you run the <b>g++</b> command and are unsuccesful with your compilation, then you might see an output that looks like this:


	hello.cpp: In function ‘int main()’:
	hello.cpp:10:1: error: expected ‘;’ before ‘}’ token
 	}


The compiler will try to give you hints on the line where the error occurs (in this case, it's complaining about line 10), and also about what the error is (in this case, a missing semicolon). You will also note that, in this case, if an error occurs, the compiler does not produce (or update) an output executable file.

If you encounter an error, use the compiler hints and examine the line in question. If the compiler messsage is not sufficient to identify the error (which happens more than sometimes), you can search online to see when the error occurs in general (or, if you are stuck, ask any of the teaching staff for help). 
To fix the error, re-open the **hello.cpp** file and edit the necessary lines.

Once you have fixed the error, run the compilation command again. <i>Debugging</i> a program code is a necessary ritual in almost all programs written (even those written by expert coders). More on that in a later class.

## Step 7: Submitting your code to Gradescope
  
You will need to turn in your correct <code>hello.cpp</code> file to Gradescope.

The lab assignment "Lab00" should appear in your Gradescope dashboard in CS 16. If you haven't submitted anything for this assignment yet, Gradescope will prompt you to upload your files.

For this lab, you will need to upload your `hello.cpp` file. You can navigate to your file, "drag-and-drop" them into the "Submit Programming Assignment" window, or even use a GitHub repo to submit your work. For now choose either of the options and follow the steps to upload `hello.cpp` to Gradescope.

If you already submitted something on Gradescope, it will take you to their "Autograder Results" page. There is a "Resubmit" button on the bottom right that will allow you to update files for your submission.

For this lab, if everything is correct, you'll see a successful submission passing all of the autograder tests and receive full credit. You can resubmit your code if you get an error: the resubmission will be available up until the Lab is due.

Congratulations on completing your first C++ program!

# Tell us about yourself

In order to get full credit for this lab, make sure to submit the Lab00 survey.
Please fill out the following form to tell us about yourself: 
<https://ucsb.co1.qualtrics.com/jfe/form/SV_1Ti1moPpMPT9PYF>. 

## Step 8: Log Out!
<strong>NOTE:</strong> If you are in the Phelps lab or in CSIL,<b> make sure to log out of the machine before you leave</b>. Also, make sure to close all open programs before you log out. Some programs will not work next time if they are not closed. Remember to save all your open files before you close your text editor.

If you are logged in remotely, you can log out using the <b>exit</b> command in UNIX:

<pre>$ exit</pre>
