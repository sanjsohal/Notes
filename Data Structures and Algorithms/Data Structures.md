Data Structures are used to store data values, relationship among them and functions that can be applied on the data values.

Time and Space complexity are metrics used to determine performance of algorithm in terms of speed and memory. Speed means how much time does it take to execute for n number of values. Memory means how much auxiliary memory does it consume to execute for n number of values.

Big O Notation is an asymptotic notation used to determine it. Following are notations of Big O starting from very high speed algorithm to low speed algorithms and these are for only one type of value N:
1. O(1)
2. log(N)
3. O(N)
4. O(N log(N))
5. O(N<sup>2</sup>), O(N<sup>3</sup>), O(N<sup>4</sup>) and so on.
6. O(2<sup>N</sup>)
7. O(N!)

When we have multiple type of values say N and M, then complexity could be like below:
1. O(M<sup>2</sup>+N)
2. O(M<sup>2</sup>+log(N))

<h3>Logarithm</h3>
Logarithm in mathematic is denoted as following:

log<sub>b</sub> x = y    if and only if b<sup>y</sup> = x

Above expression means log of x with base b = y if and only if y power of b is equal to x.

In computer science, we use logarithm as following:

log N = y if and only if 2<sup>y</sup> = N

We use above notation to denote complexity of some algorithms. We didn't put base explicitly because in computer we consider base 2 implicitly because of binary in computer science.

For e.g. log(1) = 0 if and only if 2<sup>0</sup> =1
			log(4) = 2 if and only if 2<sup>2</sup> = 4
			log(8) = 3 if and only if 2<sup>3</sup> = 8
			log(16) = 4 if and only if 2<sup>4</sup> = 16

We can see in above example when number of input N is getting doubled, power of 2 is only increasing by 1 hence log(N) complexity is better than linear complexity. Binary search is one of the example whose one of solutions have log(N) time space complexity.
