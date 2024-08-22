## Getting Started

Welcome to the VS Code Java world. Here is a guideline to help you get started to write Java code in Visual Studio Code.

## Folder Structure

The workspace contains two folders by default, where:

- `src`: the folder to maintain sources
- `lib`: the folder to maintain dependencies

Meanwhile, the compiled output files will be generated in the `bin` folder by default.

> If you want to customize the folder structure, open `.vscode/settings.json` and update the related settings there.

## Dependency Management

The `JAVA PROJECTS` view allows you to manage your dependencies. More details can be found [here](https://github.com/microsoft/vscode-java-dependency#manage-dependencies).

## What you need

We'll be concentrating on dealing with programming from the machines in the computer lab, but you will undoubtedly need to have similar software installed on a desktop or laptop at home. I would prefer that you not bring these machines to class, but rather get used to pushing updates to a GitHub repository (repo) when you change machines. But to this end, you will need to install

- git
- github classroom
- vscode
- vscode extensions for java

Links to Google Docs to help you through those should be forthcoming.

Since you're reading this, it should mean you're either on a machine in the classroom or have accomplished the above for your machine at home.

## Project 1 Instructions

This is the traditional first assignment for every new programming language. It is meant to simply accustom you to interacting with the language, the IDE, and any peculiarities of the class itself.

As we will be dealing with GitHub and VSCode, you should be starting on this assignment from a link provided to you. This should get you to the point of having a folder named HelloWorld downloaded to the machine you're working from.

## Explorer tab

On the Explorer tab, you should be able to see that the HelloWorld folder contains folders named `src` and `target`. All of your code will go under `src` and all of the machine language the compiler generates will be stored under `target`.

You should always end up with a README.md file, saved in the `src` folder. There should be subfolders `java` and `resources`. In later assignments, you may store external files in `resources`, but for now it's empty. 

Click on the subfolder to see it's actually `java\edu\guilford`. This is because we build our applications in the "space" for Guilford, `edu.guilford`. Under this, you'll find a file titled `Main.java`. Open this. Notice you now have tabs for `Main.java` and `README.md` open. Explore the menus and find `Open Preview to the Side`. This lets you see `README.md` much more like a webpage. Adjust the width of the tabs for your screen.

## Packages

Notice that in `Main.java`, it starts with `package edu.guilford`. If you were working for Microsoft, it should say `package com.microsoft`. This is just to identify your organization for now, but can be used to engineer hierarchies of classes for large-scale projects. Just put this at the head of all your files to bind them together.

## The class

The next line has `public class Main {`. The closing curly brace is on the last line of the file. Notice that these braces always come in pairs and are nested. When you type a left brace, the IDE will try to provide you with a right brace. You need to be careful about crossing them.

The word `public` means that external programs are allowed to access this part of this program. The word `class` means that when the compiler builds a program from this code, it will have a certain kind of structure. And the word `Main` is because this file is named `Main.java`. If this word doesn't match the file name, it can cause problems.

Notice that the next line is indented. If you have experience with Python, you know it enforces indentations strictly. Java does not, but it makes it much easier to read your code if you indent the code that is inside a block or enclosed in braces.

## The `main` method

The code for the next line says `public static void main(String[] args) {` - which is rather a lot. Like before, `public` means external programs can access this "method". `static` is a keyword that says this method is in some sense fixed. `void` establishes the method's return type. Remember functions in math class? Methods are like functions, and are preceded by a keyword that tells what kind of output it will have, and `void` means it won't have any output. 

The name of the method that's appearing here is `main`. This should be confusing, since the class is called `Main`, and although those are the same word, the capital M means they're totally different. If you're not a good typist, programming is a pain - capitals & lower case are different, misspellings are all different, and commas and semicolons may look alike but are totally different.

Many programs or classes will have a `main` method that it defaults to when you try to run it. In this case, everything that the program does is contained in the `main` method. Just like $f(x)$ in math class, the `(String args[])` tells you what the input of the function is. For our purposes, this won't be important, but when programs are run from the command line, they can be fed input. So if we had run this program using `java Main red blue green`, then `args` would have received three `String` arguments with the values "red", "blue", and "green". That's all stuff for later - for now, it has to be there, but you can ignore it safely.

Inside the braces of the `main` method, we have the entire executable code of the program: `System.out.println("Hello world!");`. You can treat `System.out.println` as though it were one word that says "print this", but as you might guess the `System` means it interacts with the computer system, the `out` means it's going to create output, and `println` means it's going to print a line of text.

Inside the parentheses, you'll find `"Hello World!"` or `x:"Hello World!"`. This is what is referred to as a `literal String`. The value is the part between the quotes. A `String` is a type of variable that holds words, characters, etc. In this case, we haven't saved it under a variable name, just printed it out, so it's a `literal` value. When dealing with numbers, you could refer to a literal integer, but people tend not to put the terms together. If you have `x:` at the beginning, that's VSCode telling you the name of the variable inside the `println` method - you can safely ignore this.

## Running & Debugging

OK, let's actually do something! With the `Main.java` tab active, click the `Run & Debug` button. It should make you click a button that says `Run & Debug` and then choose from a couple of options. You want `java`. If you get an error at this stage, call me over!

This should open a terminal at the bottom of your window. Here's the output mine showed: `PS C:\Users\bmarlin\Desktop\helloworld>  & 'C:\Users\bmarlin\AppData\Local\Programs\Eclipse Adoptium\jdk-17.0.8.7-hotspot\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,addrocket,server=n,suspend=y,address=localhost:61276' '-XX:+ShowCodeDetailsInExceptionMessages' '-cp' 'C:\Users\bmarlin\Desktop\helloworld\target\classes' 'edu.guilford.Main'`

`Hello world!   `

That last line is the output - the rest are just showing you what the computer does as it talks to itself. So... now you should be able to figure out what part is going to get printed. Change it to something new - put your name in it or something. Run it again.

Notice that the line ends with a semi-colon. Java doesn't really pay attention to the end of the line, so it needs that semicolon to tell it where the line ends. Position your cursor after the semicolon and hit return.

## Experimenting with the code

Now insert a new line where you tell it to print 1 + 2 * 3. Run it. It should do the arithmetic for you and get 7 - unless you put quotes around it! 

Now experiment with using `print` instead of `println`. See what difference it makes.

Now experiment with inserting `\t` or `\n` in the middle of a line of text. See what happens.

## Commenting

Insert another line. Start it with `//` and type anything after. Run it again. It should have ignored whatever was after the double slash - this is what is referred to as a comment. You should get used to putting copious comments in your code. These are notes for yourself for later or for your collaborators when you have to write code for groups. Right now, this seems like wasted effort to you, but later you'll be glad you made these notes as you try to parse out pages and pages of code!

(A friend of mine had a job working for the USGS translating code from a programming language that had not been used in decades. He spent hours trying to figure out what the original coder had been trying to accomplish and would occasionally ask me about their questionable math.) 

## Save your files!

So... there's a standard practice I want you to get into. Go up to the line after the name of the package. Insert a line and use a comment to put your name there. Insert another comment line with the date you're finishing the assignment. Every assignment needs to have this!

Now, save your file by hitting Control-S or Command-S or File > Save. While VSCode will save your file before you run it, you should get in the habit of saving it manually, too.

Now, go to the `Source Control` icon on the left (three dots and a forked path with a number over it). Click in the field that says `Message` and type a short suggestion of where you are in the project (probably "finished!"). 

 **Before** you click the button, you have to "stage changes". Hover your mouse over the line that says Changes. You should get icons that look like a page with + and - on it, a hook with an arrow end, and a plus. Click the +. Continue to each of the lines below it: most will give you a minus where the plus was above. If there are any + marks, click them.

Now, click on the button that says `Commit`. You may get a pop-up with the option `Save All & Commit Changes` or you may get a button that says "Sync Changes". This will save your changes to the repo online.

## Committing

If you have installed VSCode on a machine at home, you ought to try opening the file there as well. When you're done making changes, repeat this routine of saving and committing.

We also use the word "push" to indicate we are putting our changes on the computer into the repo. Consequently, when you get the repo contents to your machine, it is called a "pull". If you do not push when you're done and then pull on another machine, you start to have problems with differences between your versions. You may hear the term "fork" for different versions and "resolving conflicts". That is more of a topic for an advanced programming course.

## This should conclude the Hello World Project!