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

Firstly, you might want to check out the [GolfScript examples][examples], the
[builtiin references][builtins] and the [quick reference][quickref]. 

The Euclidean algorithm calculated the greatest common denominator between two
numbers `a` and `b`:

```
function gcd(a, b)
  while b != 0
    t := b
    b := a mod b
    a := t
  return a
```

Here's a
quick reference for the symbols in the GCD program:

```
;           Pop and discard top item from stack (cleanup)
'2706 410'  Raw string with two numbers on the stack (a and b)
{           New code block
  .         Duplicates the top item on the stack (t = b)
  @         Rotates the third element on the stack to the top (t, a, b)
  \         Swaps the top two items on the stack (t, b, a)
  %         Mod (t, a mod b)
  .         Duplicates the top item on the stack
}
do          Pops the stack, and if non-zero then repeat code block (we want a)
;           Pop (cleanup)
```

## Challenges

These problems are quite simple, so I'd recommend starting with them for the
code golfing.

* [Project Euler 1 - Multiples of 3 and 5][euler1]
* [Project Euler 2 - Even Fibonacci numbers][euler2]

[golfscript]: http://www.golfscript.com/golfscript/
[ruby]: http://www.golfscript.com/golfscript/
[examples]: http://www.golfscript.com/golfscript/examples.html
[quickref]: http://www.golfscript.com/golfscript/quickref.html
[builtins]: http://www.golfscript.com/golfscript/builtin.html
[euler1]: https://projecteuler.net/problem=1
[euler2]: https://projecteuler.net/problem=2
