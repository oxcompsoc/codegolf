# Code golfing

The goal of code golfing is to write the shortest possible program to implement
certain algorithms or solve a problem. 

Code golfing can be competed in any programming language you like, and you may
wish to use a language that you are familiar with. However, we will also be
playing with [GolfScript][] to write *really* short programs.

This repository contains a bunch of challenges to try in the evening.

## Setting up GolfScript

1. Head over to the [GolfScript site][] and download the interpreter for it (it
   is a Ruby script)
2. Install [Ruby][] if you haven't already
3. Create a simple example file `gcd.gs`

```
;'2706 410'
~{.@\%.}do;
```

4. Open a terminal and run `ruby golfscript.rb gcd.gs` (assuming the Ruby and
   code are in the

## So how does GolfScript work?

Firstly, you might want to check out the [GolfScript examples][examples] and the
[quick reference][quickref].

[golfscript]: http://www.golfscript.com/golfscript/
[ruby]: http://www.golfscript.com/golfscript/
[examples]: http://www.golfscript.com/golfscript/examples.html
[quickref]: http://www.golfscript.com/golfscript/quickref.html
