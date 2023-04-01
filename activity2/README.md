# Activities

## Task 1

> Refer to the following links while discussing the answer.

- What is the difference between `array` and `std::array`
  https://stackoverflow.com/questions/30263303/stdarray-vs-array-performance

//Differences between the two:

std::array is a class template that provides a number of useful member functions, such as size(), at(), and front(), while array does not provide any member functions.
std::array is a fixed-size container, while array can have a variable size.
std::array provides type safety and can be used with C++ algorithms that require iterators, while array does not provide type safety and cannot be used with C++ algorithms that require iterators.
std::array provides copy and move constructors, assignment operators, and other useful features, while array does not provide any such features.

- What is the difference between `std::array` and `std::vector`
  https://www.softwaretestinghelp.com/arrays-in-stl/

//the main differences between std::array and std::vector are:

**Size: std::array has a fixed size that is determined at compile-time, whereas std::vector has a dynamic size that can be changed at run-time.

**Memory allocation: std::array stores its elements in a contiguous block of memory allocated on the stack, whereas std::vector dynamically allocates its memory on the heap.

**Initialization: std::array is initialized using aggregate initialization syntax, while std::vector can be initialized using a variety of constructor syntax.

**Accessing elements: std::array elements can be accessed using the subscript operator [], while std::vector elements can also be accessed using iterators.

**Performance: std::array has better performance than std::vector in cases where the size of the array is known at compile-time, as it avoids dynamic memory allocation and provides cache locality.

- What is the difference between `std::list` and `std::vector`
  https://www.softwaretestinghelp.com/lists-in-stl/

//differences between std::vector and std::list:

Memory allocation: std::vector allocates a single block of memory for its elements, while std::list allocates separate memory for each node.

Random access: std::vector provides efficient random access to its elements using index-based lookups, while std::list does not.

Insertion and deletion: std::list provides efficient insertion and deletion of elements in the middle of the list, while std::vector may require expensive reallocation and copying of elements.

Iterators: std::list provides bidirectional iterators, which can traverse the list in both directions. std::vector provides random access iterators, which can be used to efficiently access elements using index-based lookups.

## Task 2

- Run the Stack and Queue examples in the following link
  https://www.softwaretestinghelp.com/stacks-and-queues-in-stl/

> make sure you correct the syntax e.g `&lt;int&gt; becomes  <int>`

```c++
#include <iostream>
#include <stack>
using namespace std;

void printStack(stack<int> mystack)
{
   while (!mystack.empty())
   {
      cout << mystack.top() << '\t';
      mystack.pop();
   }
   cout << '\n';
}

int main()
{
   stack<int> mystack;
   mystack.push(1);
   mystack.push(2);
   mystack.push(3);
   mystack.push(4);
   
   cout << "The stack mystack is : ";
   printStack(mystack);
   
   cout << "\nmystack.size() : " << mystack.size();
   cout << "\nmystack.top() : " << mystack.top();
   
   cout << "\nmystack.pop() : ";
   mystack.pop();
   printStack(mystack);
   
   return
``` 0;
}


```c++
#include <iostream>
#include <queue>
using namespace std;

void printQueue(queue<int> myqueue)
{
   queue<int> secqueue = myqueue;
   while (!secqueue.empty())
   {
      cout << '\t' << secqueue.front();
      secqueue.pop();
   }
   cout << '\n';
}

int main()
{
   queue<int> myqueue;
   myqueue.push(2);
   myqueue.push(4);
   myqueue.push(6);
   myqueue.push(8);
   
   cout << "The queue myqueue is : ";
   printQueue(myqueue);
   
   cout << "\nmyqueue.size() : " << myqueue.size();
   cout << "\nmyqueue.front() : " << myqueue.front();
   cout << "\nmyqueue.back() : " << myqueue.back();
   
   cout << "\nmyqueue.pop() : ";
   myqueue.pop();
   printQueue(myqueue);
   
   return 0;
}
```

## Task 3

- Discuss the different types of iterators present in C++. You can refer to the following link
  https://www.geeksforgeeks.org/introduction-iterators-c/

types of iterators:

**Input Iterator**: It is used to read data from a container in a sequential manner. It can be incremented using the ++ operator but cannot be decremented. Example: istream_iterator.

**Output Iterator**: It is used to write data to a container in a sequential manner. It can be incremented using the ++ operator but cannot be decremented. Example: ostream_iterator.

**Forward Iterator**: It is used to read or write data to a container in a sequential manner. It can be incremented using the ++ operator but cannot be decremented. Example: forward_list.

**Bidirectional Iterator**: It is used to read or write data to a container in both forward and backward directions. It can be incremented and decremented using the ++ and -- operators, respectively. Example: list.

**Random Access Iterator**: It is used to read or write data to a container in a random access manner, i.e., we can directly access any element of the container using the [] operator. It can be incremented and decremented using the ++ and -- operators, and we can also perform arithmetic operations like addition and subtraction. Example: vector.

These iterators can be used with the Standard Template Library (STL) containers such as vector, list, map, set, etc. to perform various operations like traversal, modification, and searching.


- What are the Benefits of Iterators
//
**Abstraction**: Iterators provide a level of abstraction that allows users to access the elements of a container without having to know the implementation details.

**Flexibility**: Iterators provide a generic interface that can be used with different containers, allowing users to write generic algorithms that work with multiple containers.

**Efficiency**: Iterators provide a way to access container elements efficiently, without having to copy or move the elements.

**Safety**: Iterators provide a safe way to access container elements, preventing users from accessing elements outside the bounds of the container.

**Range-based for loops**: The use of iterators has enabled the introduction of range-based for loops in C++11, which simplifies the syntax for iterating over the elements of a container.

## Links

- https://cpp.sh/
