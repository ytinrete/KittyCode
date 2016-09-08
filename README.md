# KittyCode
toy code for fun

This is some kind of rules and functions to encode and decode string.

For example:

KittyCode->encode->喵◎唔喵☆呜喵★◎喵★◎喵★呜喵◎○喵☆～喵☆◎喵☆●喵
Hello World->encode->喵◎。喵☆●喵☆昂喵☆昂喵☆～喵◇※喵●★喵☆～喵★◇喵☆昂喵☆◎喵


The rules are simple:
Every character from the text will be encode to some strings.
Then it will be grouped and divided by "喵".
The encode methods are:
1.Get the 16 based unicode of the character "uni16".
2.Translate every single words in "uni16" by the following map:
0  ※  8251   203b
1  △  9651   25b3
2  ◇  9671   25c7
3  ○  9675   25cb
4  ◎  9678   25ce
5  ●  9679   25cf
6  ☆  9734   2606
7  ★  9733   2605
8  。  12290  3002
9  呜  21596  545c
a 哒  21714  54d2
b 唔  21780  5514
c 昂  26114  6602
d ！  65281  ff01
e ？  65311  ff1f
f ～  65374  ff5e
3.Put them all togeter and you'll get the result strings which represent the encode character.

This program is how to do encode and decode using js.
