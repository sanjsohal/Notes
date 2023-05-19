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

<h3>Arrays</h3> 
In some programming languages, arrays can be both static and dynamic like Java or Python. But on the other hand in javascript, there is no concept of dynamic arrays. 

Static Arrays are used to store fixed number of elements. When we store n number of elements in an array. Our computer looks for n number of contiguous auxiliary memory locations to store that array. 

For e.g. Let us say there is an array of size 2. Suppose our operating system start saving elements from memory index 3 and each integer is of 64 bit. Let us consider each memory slot is of 1 byte i.e. 8 bits. Now first element will save from memory slot 3 to memory slot 11, second element will save on memory slot 12 and end on 18 and same way third element will occupy memory slot of 19 to 27. 

1. Why get operation just takes O(1) time to fetch an element from any index no matter how big it is?
	Because our operating system know where does first element stored of array. So let us say we want to fetch third element of array i.e. array[3] As our operating system knows first element at 3 and each integer is of fix size 64 bits, it will simply fetch the element in O(1) time by making this calculation = 3+2(index of element to fetch) X 8 i.e. 3+16=19 that is where our third element is stored. Same way when we use set operation to replace an element at Nth position, it also have time complexity of O(1). In simple words, get and set operation has space and time complexity of O(1).

			get operation = O(1) Time and Space Complexity
			set operation = O(1) Time and Space Complexity

2.  Time and space complexity for initiliazing an array of fixed size is O(N). Let us suppose that we want to create an array of 6 integers(64 bit integer). Then our computer will look for 6 contiguous locations on memory to allocate space to this array. So it will take O(6.N) space and time. In asympotatic notation, 6 is considered not significant. Hence time and space complexity is O(N).

					initialize operation = O(N) Time and Space Complexity

3. Time complexity of traversing an array is O(N) where N is number of elements in array. As traversing an array didn't require space, so space complexity of traversing is O(1) while traversing an array.
					Traversing array without performing any auxiliary opation on element= O(N) Time complexity and O(1) Space Complexity

4. Space and time complexity for copy operation is O(N)
5. Insert operation is used in case of Dynamic Arrays. Dynamic arrays are arrays whose size can increase dynamically. In Java, ArrayList and Vector are two implementations of Dynamic Array. If we declare an arraylist without giving size. It creates arraylist of size 16. Let us suppose if we are inserting element at last position, it will take O(1) time and space. But if array is full then and we try to insert other element, it will create a new array in O(N) time and O(1) space. Space is O(1) because it will wipe out the earlier space.

Note: Insert operation is different from set operation as set operation is used to override existing value and with insert operation, we can insert element at any position whether it is start, end or anywhere in middle of array.

