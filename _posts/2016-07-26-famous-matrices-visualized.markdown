---
layout: post
title:  "Famous Matrices Visualized"
date:   2016-08-1 16:35:10 -0400
categories: octave math
---

Hello World!

I started playing around with Octave a little while ago while taking a course on [machine learning](https://www.coursera.org/learn/machine-learning/)(highly recommend). There was a function called magic(n) which would generate(or look up) an n by n matrix that would satisfy this condition:

*All Rows, Columns, and Diagonals add up to the same value.

If this sounds like sudoku, its because it is! Magic squares have been around for a long time, often as symbols of superstition or.. well, magic. So what does a 3x3 magic square look like?

It's worth noting that there are only 8 possible 3x3 magic squares, and they are all reflections or rotations of this one, also known as the ["Lo Shu Square"](https://en.wikipedia.org/wiki/Lo_Shu_Square).




{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}