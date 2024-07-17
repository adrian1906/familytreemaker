familytreemaker
===============

This program creates family tree graphs from simple text files.

The input file format is very simple, you describe persons of your family line
by line, children just have to follow parents in the file. Persons can be
repeated as long as they keep the same name or id. An example is given in the
file `LouisXIVfamily.txt`.

Important Note:
There needs to be at least 2 blank lines between families.

Families require 2 parents - If one parent is not known, use a placeholder

The code is hard coded for 5 generations, that number can be changed.

This code produces the dot syntax to use with GraphVIZ to produced the visual trees.

I played around with this code for about a week and learned a great deal about GraphVIZ because of it.
I've since moved on to a more powerful family tree repo: https://github.com/gramps-project/gramps


Installation
------------

Simply clone the repo.

This script outputs a graph descriptor in DOT format. To make the image
containing the graph, you will need a graph drawer such as [GraphViz] [1].

[1]: http://www.graphviz.org/  "GraphViz"

Usage
-----

The sample family descriptor `LouisXIVfamily.txt` is here to show you the
usage. Simply run:
```
$ ./familytreemaker.py -a 'Louis XIV' LouisXIVfamily.txt | dot -Tpng -o LouisXIVfamily.png
```
It will generate the tree from the infos in `LouisXIVfamily.txt`, starting from
*Louis XIV* and saving the image in `LouisXIVfamily.png`.

You can see the result:

![result: LouisXIVfamily.png](/LouisXIVfamily.png)
