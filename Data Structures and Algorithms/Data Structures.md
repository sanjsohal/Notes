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
5. To copy an array, it takes O(N) space and time complexity.
6. Insert operation is used in case of Dynamic Arrays. Dynamic arrays are arrays whose size can increase dynamically. In Java, ArrayList and Vector are two implementations of Dynamic Array. If we declare an arraylist without giving size. It creates arraylist of size 16. Let us suppose if we are inserting element at last position, it will take O(1) time and space. But if array is full then and we try to insert other element, it will create a new array in O(N) time and O(1) space. This is a special case scenario when array is full and we try to insert new element it takes O(N) time. Amortized analysis is used to determine the complexity for scenarios which are not frequent. Space is O(1) because it will wipe out the earlier space. If we need to insert an array at start position, time complexity is O(N). 

Note: Insert operation is different from set operation as set operation is used to override existing value and with insert operation, we can insert element at any position whether it is start, end or anywhere in middle of array.


<h3>LinkedLists</h3> 
LinkedList is conceptually same as Arrays. The only difference is whereas arrays store the data in contiguous locations, linkedlist don't store data in contiguous locations. It can have different elements stored at totally different locations and not in continous locations like arraya. Elements are connected with linking between them.

1. O(i) is time complexity to get ith element in linkedlist and O(1) is space complexity as we don't use any space for this operation.
2. O(i) is time complexity to set element at ith position in linkedlist and space complexity is O(1).
3. To initialize a linkedlist, time and space complexity is O(N).
4. To copy a linkedlist, time and space complexity is O(N).
5. To insert an element at any position in linked list, time and space complexity is O(1).

Note: LinkedLists has many types. Single linked list is the one in which one element is connected to other in forward direction. Double linked list is the one in which each element has reference to next element and previous element. Circular linked list is a list in which head and tail element is connected with each other.

<h3>Hashtable</he> 
Hashtables are used to store data in form of key and values. Underlying structure used by hashtables is an array where each index of array furthur contain a linkedlist. To store data in hashtable, first some hashcode is calculated on basis of some hashing function to calculate the index to store the value. If at some point, same value is returned by hashing function(hash collision) then data is stored furthur in the linkedlist with the key. If a good hashing function is used, then there is very less chance of hash collision.

1. insert, search and deletion of an entry from hashtable is performed in O(1) ususally.
2. Let us suppose if the underlying structure is about to become full or it is 2/3 occuppied, then a new array is copied and elements are stored at different location as per new hash position calculated according to the size of underlying array. Here as per amortized analysis, time and space complexity becomes O(N).


<h3>Stacks and Queues</h3>
Stacks are one of the very simple data structure. It is a LIFO data structure. LIFO stands for Last In First Out. Element can be inserted from the end of array and removed from end of array. Stack of books is an example of stack. Underlying data structure used by stack is dynamic array. Following are the operations that can be performed in stack:

1. push: This operation is used in insert an element in stack and can be performed in O(1) time and space complexity.
2. pop: This operation is used to remove an element from stack and also can be performed in O(1) time and space complexity.
3. peek: This operation is used to read the last element from tack. It can be done in O(1) time and space complexity. This operation doesn't remove the element but only read from the stack.
4. search: This operation can be done in O(N).

Queues are also simple data structures. It is a FIFO data structure. FIFO stands for First In First Out. A queue of people on booking center is an example of queue. Underlying data structure used in queue is a linked list. Following are the operations can be performed in queue:

1. enqueue: It is used to insert an element. Space time complexity is O(1)
2. dequeue: It is used to delete an element. Space time complexity is O(1)
3. search: Space time complexity is O(N)



<h3>Strings</h3>
Strings are array of characters. In java and some other languages, strings are immutable. It means a string cannot be altered once it is created. Various operation and time space complexity for performing that operations is:

1. traverse: For traversing a string, time complexity is O(N) and space complexity is O(1) if we are not performing any auxiliary operation.
2. copy: Copy operation takes O(N) time space complexity.
3. get: This operation can be performed in O(1) time space complexity.
4. If we want to concatenate two strings of length N and M. Time space complexity is O(N+M) for such operation.

Note: For above last point, it is adivisable to convert string to array of characters, if we want to perform concatenation operation as we can insert element in O(1) time space in growable dynamic array. If array has become full, then only it takes O(N) time because in that situtation, a new array is created and elements are copied to that one. So this becomes case of amortized analysis as this happens very rarely.


<h3>Graphs</h3>
Graphs are one of non linear data structure. They are collection of nodes and these nodes may or may not connect with each other. Nodes of graph are also called vertices or vertex. Connection between these vertices are called edges. There are following types of graphs.
1. A graph is said to be connected if we can reach to every other vertex from one vertex through edges. 
2. If in a graph there are vertexes which cannot be reached from other vertexes. That graph is called disconnected graph.
3. A graph is said to be directed graph if there is a direction between nodes. For e.g. a graph of flights between different places of world is directed graph.
4. On the other hand, a graph is said to be undirected graph when there is no direction of edges between nodes or vertexes. For e.g. Friendship network of people don't have any direction. So the friendship network is an example of undirected graph.
5. A graph is said to be cyclic graph if it has three or more edges and have kind of closed cycle of edges between them. 
6. A graph is said to be acyclic graph if it doesn't have closed cycle between three or more vertexes.

Note: When writing algorithm for cyclic graph, please make sure that you don't write which put your program in infinite loop. There should be some way to mark the visited nodes.

Some applications of graph data strucutre are:
1. Storing products in ecommerce applications.
2. Storing route data for a food delivery app.
3. Flights network of world

Operations that can be performed on graph are:
1. For storing a graph, it takes O(V+E) space complexity where V is number of vertexes and E is number of edges that are connections between vertexes.
2. traverse: There are two ways to traverse a graph that are depth first search technique and breadth first search.


<h3>Trees</h3>

A tree is also a non linear data structure which is kind of graph and has root node. Following are some properties of trees:
1. A tree is an acyclic graph.
2. Each node can have only one parent node.

There are following types of trees:
1. Binary tree: A binary tree is a tree where a node can have atmost two child nodes.
2. Ternary tree: A ternary tree is a tree where a node can have atmost three child nodes.
3. k-ary tree: A tree where a node can have atmost k number of child nodes is called k-ary tree.

Operations that can be performed on tree are:
1. store: For storing a tree, it takes O(N) space complexity where N is number of nodes in tree.
2. traverse: Traversing through a tree takes O(N) time if we are not performing an auxiliary operation.
