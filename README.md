# Undefined Behavior After Clearing a Vector in C++
This repository demonstrates a common error in C++ when using `std::vector` and iterating after clearing it.

## The Bug
The code in `bug.cpp` attempts to access elements of a vector after it has been cleared. This leads to undefined behavior because the vector's size is zero, but the loop still tries to access elements.

## The Solution
The solution, shown in `bugSolution.cpp`, avoids this error by checking if the vector is empty before attempting to access its elements.

## How to Run
1. Clone the repository.
2. Compile the code using a C++ compiler (e.g., g++):
   ```bash
   g++ bug.cpp -o bug
   g++ bugSolution.cpp -o bugSolution
   ```
3. Run the executables:
   ```bash
   ./bug
   ./bugSolution
   ```
The `bug` executable will likely crash or produce unpredictable output. The `bugSolution` executable will output correctly.