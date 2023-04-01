# Activities

---

> [Course Feedback](https://ojp.metropolia.fi/lomakkeet/1/lomake.html?code=VFQwMEZFMzktMzAwMQ==)

---

## Task 1

- What is the difference between function overloading and function templates. You can refer to the programs in the `./src/` folder as well as [Links 2 and 3](#links) below.

//
Function overloading is a technique in which multiple functions can have the same name, but different parameters. The compiler distinguishes between the functions based on the number, types, and order of the parameters. The implementation of each function can be different, but they must have the same name. This allows the programmer to create functions that have the same name, but can perform different tasks based on the input parameters.

Function templates, on the other hand, are a way to create generic functions that can handle multiple types of input. Instead of defining a function for each data type, a single function template can handle multiple data types. The template parameters are specified in angle brackets <>, and the function definition uses these parameters as placeholders for the actual data types. When the function is called, the actual data types are substituted for the template parameters, and the function is compiled for each specific data type.



- Rewrite the following program using templates

```cpp
#include <iostream>

int add(int x, int y)
{
    return x + y;
}

double add(double x, double y)
{
    return x + y;
}

int main()
{
    std::cout << add(1, 2); // calls add(int, int)
    std::cout << '\n';
    std::cout << add(1.2, 3.4); // calls add(double, double)

    return 0;
}
```
```c++
#include <iostream>

template <typename T>
T add(T x, T y)
{
    return x + y;
}

int main()
{
    std::cout << add(1, 2); // calls add<int>(int, int)
    std::cout << '\n';
    std::cout << add(1.2, 3.4); // calls add<double>(double, double)

    return 0;
}
```

## Task 2

Refer to the following link:
https://www.softwaretestinghelp.com/vectors-in-stl/

Discuss the difference between

- Size() and capacity()

// The main difference between size() and capacity() is that size() returns the actual number of elements stored in the vector, while capacity() returns the maximum number of elements that can be stored in the vector without resizing.

- begin() and cbegin()

//The difference between begin() and cbegin() lies in their constness. cbegin() returns a constant iterator, meaning that the elements pointed to by the iterator cannot be modified, whereas begin() returns a regular iterator, which allows modification of the elements.

- end() and cend()

//The main difference between end() and cend() in C++ STL vectors is the constness of the iterators they return.

end() returns an iterator that points to the element one past the last element in the vector. This iterator can be used to access and modify elements in the vector.

cend() returns a const iterator that also points to the element one past the last element in the vector. This iterator can be used to access the elements in the vector, but cannot be used to modify them.

In other words, end() returns a non-const iterator that can be used to modify the vector, while cend() returns a const iterator that can only be used to read the vector.

## Links

1. https://cpp.sh/
2. https://www.learncpp.com/cpp-tutorial/function-templates/
3. https://www.learncpp.com/cpp-tutorial/function-overload-differentiation/
4. https://www.geeksforgeeks.org/design-and-analysis-of-algorithms/
