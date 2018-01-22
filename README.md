# Singletrack Gray Codes
## Gray Codes are a form of binary where only one bit changes between subsequent numbers.
## Singletrack Gray Codes achieve this with multiple sensors reading a single track.

[The Wikipedia article for gray codes has a section for singletrack gray codes.](https://en.wikipedia.org/wiki/Gray_code#STGC)

This page shows an implementation of singletrack gray codes using a prime number of sensors.
The number of sensors determines the number of bits for the resulting codes.
With a prime number of sensors N, the algorithm used here will generate 2^n - 2 values.
So
- 30 values using 5 sensors
- 126 values using 7 sensors

The Javascript implementation works for up to 19 sensors.  Beyond that runs into some resource limitations.
The algorithm is fairly direct and is therefore pretty quick.

The webpage only allows one to choose from 3, 5 or 7 sensors.  11 sensors result in 2046
values which is just too many to be able to step through them or even see what is going on
with the graph.

The graph rotates the 3, 5 or 7 sensors within the single track.  Try figuring out which 
bit will change next (there is a clockwise and counter-clockwise rotation button).  The
bottom three sensors and bits are color coded.  You should be able to figure out the rest.

As you can tell from the Wikipedia article, Norman Spedding, Hiltgen, Paterson and Brandestini
figured out this stuff about 20 years before me.  I figured this out on my own with the 5
sensor result informing me.  I went through a few algorithms before figuring out the implemented
one. 

I'd like to figure out well performing algorithms for non-prime number of sensors.  Per the
article above, if n is a power of 2, there will be a pattern that yields 2^n - 2n values.
In addition, they say that there is a singletrack pattern that will yield 360 values from 
9 sensors.

[Try out the page](http://htmlpreview.github.io/?https://github.com/JaySpencerAnderson/Singletrack/blob/master/prime.html)
