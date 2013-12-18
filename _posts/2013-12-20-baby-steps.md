---
layout: post
title:  "Baby Steps: Console and Artificial \"Intelligence\""
date:   2013-12-20 11:17:00
categories: evolution gaming dev
---

When you start coding, your entire world can change in little time. Or at least that happened for me. I can only describe it like being in
opposite sides of a thick wall:

* On one side all you can see is the result: programs, websites, Operating Systems, yadda, yadda, yadda. 
* On the other side though, you can see the clockwork of all that, and by seeing it, you can *understand* what's going on! You begin to appreciate the quality of 
the structures, the speed, the design, and the challenge that it must have demanded from the developers. 

It's how I think the cooks probably can appreciate food better than most of us who can barely make a sandwich.

#Baby Steps

##Gooey??

When I started coding, I did a lot of basic programs, and that felt great. But the first one I really enjoyed was this little project in college. We've got to write
a program that let the player:

* Play a game of [Sudoku](http://en.wikipedia.org/wiki/Sudoku).
* Resume a previous game.
* Show the mistakes.
* Keep a Score

Pretty basic thinking of it now, but back then was a serious challenge. My friend (and classmate) Fernando Minardi (who I will call *Fer* from here) was my partner in 
the project, and we decided to give the player a [GUI](http://en.wikipedia.org/wiki/Graphical_user_interface) *(graphical user interface)* (it wasn't *necessary* for 
the evaluation, but we wanted to "get our hands dirty"). We started coding and it was really fun! It ended up like this (it's in spanish since I live in Paraguay!):

![][sudoku]

I won't lie... I don't like it that much either. But back then it was *AWESOME!!* ... Man!! our first GUI!! And it does what it's supposed to do!! (it didn't crash
randomly like our first attempts!). We were happy, and run to show my family (we finished the program in my house) how amazing this was. With tears of joy in our eyes
we went to the dining room, laptop in our hands, and showed them! :'D .... The reaction was this:

*This... is..... hmmmm... niiiice* (read with the least convincing voice you can imagine). 

That's when I first realized it wasn't easy to get other people excited about this kind of stuff. Sure, it wasn't Crysis or Uncharted, but it was *hard* to make. But
among our classmates, our program was one of the best.

##OK, now make it *think*

Our next gaming-related assignment (Fer was *always* my partner during college, and we both love games!) was *Batalla Naval ++*, an implementation of 
[Battleship]( http://en.wikipedia.org/wiki/Battleship_\(game\) ) with some modifications:

* 2 levels for each player (surface and submarine)
* The player has 2 submarines (3 squares) and can move them, sink them or put them in the surface.
* If a submarine is damaged, automatically goes to the surface.
* New Tools:
    * **Spy Aircraft** (2): the player selects a row, a column, or a diagonal, and can see everything in there for a turn.
    * **Spy Bomb** (3): the player selects a square, and the spy bomb shows everything in there for three turns.
    * **Ballistic Missile** (&infin;): the one from the original game, you select a square, shoot, and if hits, it's your turn again.

And the program must fulfill these requirements:

* The use of `conio.h`, a Windows library for console interfaces ( no GUI this time :'( )
* AI .... **ARTIFICIAL INTELLIGENCE** (OMG!! Our program must *play* against a human player! *A W E S O M E !!!*.

So, we started playing on paper the modified version of the game, and thinking about some strategies for the AI, and we ended with a nice one, which was pretty clever. 
We started with the airplanes, and then the bombs, and then firing at everything that we found, this is one of the spying layouts, it maximizes the spied area:

    |a|_|_|_|X|X|X|_|_|b|
    |_|A|_|_|X|E|X|_|B|_|
    |_|_|X|_|X|X|X|X|_|_|
    |X|X|X|X|_|_|X|_|_|_|
    |X|E|X|_|X|X|_|X|X|X|
    |X|X|X|_|X|X|_|X|E|X|
    |_|_|_|X|_|_|X|X|X|X|
    |_|_|X|_|_|_|_|X|_|_|
    |_|X|_|_|_|_|_|_|X|_|
    |X|_|_|_|_|_|_|_|_|X|

And it looked like this:

![][battleship]

Writing those program was incredibly fun!! We were learning a lot about coding, and we felt very proud when our own game was beating us 9 of every 10 matches (sometimes,
if the CPU was given the first turn, it could play a perfect game, and beat you at the second turn!)

> Note for geeks:

You can download Sudoku's Source from [here](https://github.com/torresmateo/TAI1-Sudoku), and Batalla-Naval from [here](https://github.com/torresmateo/Batalla-Naval)

Both programs were written in C, and in *ONE FILE* per project (`main.c`)... I know, that's wrong. But hey!!, we were absolute beginners!!

[sudoku]:/images/baby-steps/sudoku.png "Our First GUI!!"
[battleship]:/images/baby-steps/battleship.png "Our First AI!!"
