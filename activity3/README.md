# Activities

## Task 1

- What are the advantages of the C++ Standard Template Library (STL):
1. Increased productivity and efficiency due to the use of pre-built, generic containers and algorithms.
2. Standardization and portability of code across different platforms and compilers.
3. Reduced development time and cost due to the availability of well-tested and optimized code.
Supports a wide range of container types, algorithms, and iterators for various data structures and operations.

- What are the disadvantages of STL?
1. Overhead of learning and understanding the library.
2. Use of templates can lead to longer compile times and larger binary sizes.
3. Limited flexibility in terms of customization and optimization compared to writing custom code.

- What are the main components of STL?
1. Containers: Data structures that hold a collection of elements.
2. Algorithms: Pre-built functions that operate on containers.
4. Iterators: Generalized pointers that provide a way to traverse elements in a container.
3. Function Objects: Objects that act like functions, often used with algorithms to customize their behavior.

> You can refer to the following link: https://www.geeksforgeeks.org/the-c-standard-template-library-stl/

## Task 2

- Refer to `./src/non-manipulative.cpp`
  - Discuss how the program works
This program demonstrates the usage of various functions provided by the C++ Standard Template Library (STL) for manipulating vectors.
The program first initializes a vector 'vect' using an array 'arr' and then displays its elements using a for loop.

  - What are the Non-Manipulating Algorithms used in the program?

1. max_element(vect.begin(), vect.end()): It returns an iterator pointing to the largest element in the range [vect.begin(), vect.end()].

2. min_element(vect.begin(), vect.end()): It returns an iterator pointing to the smallest element in the range [vect.begin(), vect.end()].

3. accumulate(vect.begin(), vect.end(), 0): It returns the sum of all the elements in the range [vect.begin(), vect.end()], starting from an initial value of 0.

- Refer to `./src/manipulative.cpp`
  - Discuss how the program works
  The program initializes a vector with an array of integers, prints the original vector, erases the element with value 10 from the vector using the erase() function and then prints the updated vector. It then removes the duplicate elements from the vector using the unique() function followed by erase() function and prints the final updated vector.

  - What are the Manipulating Algorithms used in the program?
erase is used to remove an element from the vector. In this program, it is used to remove the element with value 10 from the vector.
unique is used to remove consecutive duplicates from the vector. In this program, it is used to remove the duplicate value 20 from the vector.

> You can refer to the following link: https://www.geeksforgeeks.org/c-magicians-stl-algorithms/

## Task 3

- Refer to the following article. Reflect on the difference between Big Oh and little oh
  https://www.baeldung.com/cs/big-o-vs-little-o-notation

//The article explains the difference between Big O and Little o notation. Both notations are used to describe the time complexity of algorithms. Big O notation describes the worst-case scenario for an algorithm, while little o notation describes a tighter upper bound for the growth rate of the algorithm. In other words, an algorithm with a growth rate of O(n) can be said to have a growth rate of o(n^2), but the reverse is not true. Big O notation is used to provide an upper bound on the worst-case complexity of an algorithm, while little o notation is used to provide a tighter upper bound on the complexity of an algorithm.  

## Task 4

Refer to one of the following articles. Reflect on the differences between Big Oh, Big Omega and Theta.

Big Oh, Big Omega, and Theta are all notations used to describe the growth rate of functions. Big Oh notation is used to describe the upper bound of a function, which means that it represents the worst-case scenario of the function's growth rate. Big Omega notation is used to describe the lower bound of a function, which means that it represents the best-case scenario of the function's growth rate. Theta notation, on the other hand, is used to describe the tight bound of a function, which means that it represents the average-case scenario of the function's growth rate.

In simpler terms, Big Oh represents the maximum time complexity of an algorithm, Big Omega represents the minimum time complexity of an algorithm, and Theta represents the average time complexity of an algorithm. These notations are useful in analyzing the efficiency of algorithms and determining which algorithm is the best for a particular problem.

- https://jarednielsen.com/big-o-omega-theta/
- https://www.codeandgadgets.com/big-oh-big-omega-and-theta-definitions/
- https://www.geeksforgeeks.org/difference-between-big-oh-big-omega-and-big-theta/
