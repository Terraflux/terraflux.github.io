---
layout: post
title:  "Famous Matrices: Magic Squares"
date:   2016-08-1 16:35:10 -0400
categories: octave math
---

Hello World!

I started playing around with Octave a little while ago while taking a course on [machine learning](https://www.coursera.org/learn/machine-learning/)(highly recommend). There was a really cool function I found called magic(n) which generates an n by n matrix that satisfies this condition:

- All Rows, Columns, and Diagonals add up to the same value.

If this sounds like sudoku, its because it is! Magic squares have been around for a long time, often as symbols of superstition or.. well, magic. So what does a 3x3 magic square look like?

![LoShuSquare]({{ site.url }}/assets/LoShuSquare.png)

It's worth noting that there are only 8 possible 3x3 magic squares, and they are all reflections or rotations of this one, also known as the ["Lo Shu Square"](https://en.wikipedia.org/wiki/Lo_Shu_Square). GNU Octave has a suite of visualization functions which I'll be referencing along the way. For example, here is an imagesc() rendering of the Lo Shu Square, in grayscale with a colorbar:

![loshugray]({{ site.url }}/assets/loshugray.png)

So what would a 5x5 magic square look like?

![5sc]({{ site.url }}/assets/5sc.png)

It looks like a pattern might be starting to emerge. Here's the sequence of squares from 6-10.

![6sc]({{ site.url }}/assets/6sc.png)
![7sc]({{ site.url }}/assets/7sc.png)
![8sc]({{ site.url }}/assets/8sc.png)
![9sc]({{ site.url }}/assets/9sc.png)
![10sc]({{ site.url }}/assets/10sc.png)

Several patterns seem to be differentiating in the sequence. Squares whose size is an odd number tend to take on tesselating diagonals, while even squares seem to adopt a checkboard approach. Also worth noting, the highest number required to complete the square increases at exponential time. A magic square of N size requires N^N to be its largest number. This becomes a computational hurdle pretty quickly, at around n=100, the program begins to complain. So here's n=90-92, colorized and along with a new 3d visualization function(surf()):


![90sc]({{ site.url }}/assets/90sc.png)
![90surf]({{ site.url }}/assets/90surf.png)
![91sc]({{ site.url }}/assets/91sc.png)
![91surf]({{ site.url }}/assets/91surf.png)
![92sc]({{ site.url }}/assets/92sc.png)
![92surf]({{ site.url }}/assets/92surf.png)

Neato! Unfortunately, the function returns the same square for each of its calls on the same input so in all likelihood it is some sort of look up table. However I wonder at this point if the patterns and strategies witnessed are more a choice of the function that generated these squares for simplicity, or an implicit constraint about how magic squares can be constructed. If a n=91 could be reconstructed to look like an n=90, or vica versa, then we could be sure(ish) there were no true constraints on magic square construction patterns of arbitrary size.

At this point, I was ready to say I was done with this little article but then I discovered [this](https://www.gnu.org/software/octave/doc/v4.0.1/Famous-Matrices.html) lovely little function. Soooo I'll be back with more articles! (and matrices)