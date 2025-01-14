# IOKranf

Educational library in Javascript that is great for kids to learn programming. 

This library emulates a "console" with simple println and input command. 

This javascript library is inspired by the great C's <iostream.h> library. 

The actual code of the IOKranf library is a mixture of several projects:
* IOCream library: https://bitbucket.org/sumukhbarve/iocream/
* Promise-Alert project: https://github.com/rBurgett/promise-alert
* The "co" package: https://www.npmjs.com/package/co

Thanks for the many contributors to these projects: Without them this library would not exist!

ioKranf.js is a simple library, allowing you to easily port your console-based code to Javascript and run it in a browser of your choice. 

Using ioKranf.js, all programs/projects written during any introductory course to Computer Science, irrespective of the language used or rigor, can be QUICKLY and ELEGANTLY rewritten in Javascript. The primary intention of this library is to encourage new programmers to explore coding, and to engage in prototype-based programming.


# Why still another educational library to learn how to code?

I wanted a quick and easy way to teach how to code to my 3 kids (Cassian, Darian and Lara).

Initially, I started using Python but there are several things that kept me away from Python:
* The Python syntax wasn't the easiest one for the kids (especially the "for" loops).
* Another thing that profoundly bothered me with Python is that we spent more time in learning how to run the libraries written by others (giving the proper parameters in the right order,etc.) than we were spending time in actually learning algorithms, code complexity (O(N)) of algorithms, etc. and, in general, how to create good code.
* The coding environment in Python is terribly and horribly bloated (a complete Python environment often takes more than 1GB of hard drive space)!
* I wanted an easy debugger where you can execute step-by-step the instructions, with a "watch" window to see the variables "moving" and this was not easy to setup in Python (are there any good debugger in Python?).
* I wanted a programming environment that was directly available to everybody, everywhere on the planet.

Then, I tried to use the "scratch" programming language. "Scratch" is a nice language for the very young. But, when your kids are around 10-12 years old, you want to teach them how to create "good" code: You want to talk with them about algorithmics, procedural programming, data structures,etc. ...And "Scratch" is not a good idea for that (i.e. Writing a "quicksort" in scratch is a headache!).

Thereafter, I found the excellent "iocream" library. It almost solved all the issues detailed here above ...but this library is still very cumbersome in the way you need to write the "input" functions: i.e. you need to use "call-back" functions and this adds an extra layer of un-needed complexity to your code that makes your code very difficult to understand for the younglings. So I rewrote the "input" functions from the "iocream" library to make them much easier to use "et voilà!" the "IOKranf" library was born! Enjoy!


# What's the advantage of using this library to learn how to code?

The IOKranf library has the following advantages: 
* It offers to code in a progamming language with a very easy syntax (the syntax of Javascript is very easy!) 
* It offers a great debugger (the one integrated in Firefox is really good!)
* It's accessible everywhere easily (because everybody has Firefox or Chrome installed!)
* It's not bloated: it's a single 15KB file! The only required file is the file "lib/iokranf.js". There are no dependencies to any third-party library (such as jQuery, Angular,etc.). 
* This library is very simple to use: You only need to learn the Javascript syntax any nothing else. No need to learn the syntax of any third-party complex & cumbersome library (such as jQuery, Angular,etc.). In this way, you can really focus on what really matters: algorithmics, data structure, clever code.
* To edit your code you can use any text editor (e.g. notepad) but i suggest you to use <a href="https://code.visualstudio.com/">Visual Studio Code</a> because it's the best Javascript editor: It's 100% free and it has code-completion, syntax-coloring and even a very nice javascript debugger directly accessible inside.

In the forecoming years, i intend to post many examples of usage: sorting algorithms, searching algorithms, graph algorithms, etc.

Don't forget to "star" this repository to get an update when I'll be adding new content!


# Quick Start Guide

The library gives access to a few different functions. The most important ones are:
```
  io.println()    : Prints a message inside the "console".
  io.printhr()    : Prints a large horizontal bar inside the "console".
  yield io.input(): Creates a inline input box inside the "console"; the user must hit Enter to submit the input.
  yield io.click(): Creates a horizontal list of buttons for the user to click on.
  yield sleep(ms) : Sleep ms milliseconds (and refresh the screen during sleep).
  io.clr()        : Clear all text inside the "console".
  io.close()      : If your program has finished, you can clearly indicate that by calling close().
```

Here is a small JavaScript demonstration program (it's really self-explanatory!):
```
  io.println('Hello!');
  io.printhr();
    
  io.println('Are you happy?!');
  var r=yield io.click('yes','no');
  io.println('you clicked '+r+'\n');
	
  var s=yield io.input('Enter your name:');
  io.println('Hello '+s+'\n');
  io.close();
```

Here is a video-screen-capture of the execution of the above program:
![demo_gif](https://github.com/Kranf99/IOKranf/blob/main/demo.gif)

You'll get more documentation (although a little bit outdated) <a href="https://bitbucket.org/sumukhbarve/iocream/src" target="_blank">here</a>.

# The Demos and Examples

Inside the "demos" directory, you'll find a few games made with the IOKranf library:
* A simple text-based adventure in the same spirit of <a target="_blank" href="https://en.wikipedia.org/wiki/Zork">Zork</a>: <br>
  See the file "[zork_mini.html](demos/zork_mini.html)" (or "[zork_mini_FR.html](demos/zork_mini_FR.html)" for the french version).
  
* A simple "Tron/Snake" game: <br>
  See the file "[tron.html](demos/tron.html)"
  
* A simple variation of the "Tetris" game.<br>
  To create this game, we wrote first several "intermediary", simpler projects:
   - "[draw_square_v1.html](demos/draw_square_v1.html)" (or "[draw_square_v1_FR.html](demos/draw_square_v1_FR.html)" for the french version).
   - "[draw_square_v2.html](demos/draw_square_v2.html)" (or "[draw_square_v2_FR.html](demos/draw_square_v2_FR.html)" for the french version).
   - "[simple_tetrisk_v0.html](demos/simple_tetrisk_v0.html)"
   - "[simple_tetrisk_v1.html](demos/simple_tetrisk_v1.html)": This project already does everything what the final "[tetrisk.html](demos/tetrisk.html)" project does but the code can be improved.
   
  The final "Tetromino" game is inside the file "[tetrisk.html](demos/tetrisk.html)" (or "[tetrisk_FR.html](demos/tetrisk_FR.html)" for the french version).
  This "Tetromino" game is complete & playable: It has music, soundfx, display of next piece, high score.
  Furthermore, it works in all browsers that supports a keyboard (i.e. you need the "arrow keys" to move the tetromino)!
  And it's really fun to play!
  
  Possible improvements: 
   - add a "hold" key and a "hard drop" key 
   - implement the <a target="_blank" href="https://tetris.fandom.com/wiki/Random_Generator">7-bag Random Generator</a>
   - show a <a target="_blank" href="https://tetris.fandom.com/wiki/Ghost_piece">ghost piece</a>
   - <a target="_blank" href="https://tetris.fandom.com/wiki/Tetris_Guideline">add T-Spin, a lock-delay (difficult!).</a>
   
* A fast Mental Calculation game where you need to compute an addition in a limited amount of time.<br>
  See the file "[Mental_calculation.html](demos/Mental_calculation.html)"
  
# Closing notes.

The library is under "MIT License", so that anybody can use it for free!<br>
Don't hesitate to contact me if you want to propose some improvements to the libary!<br>
Have fun!

Frank
