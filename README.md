
![logo](/resources/tutelogo.png)

## <div align="center">Tutorial 03</div>

## Objectives : Learn to use Structures and Reference type parameters

Use your Repl.IT account and use the Instructions provided by your Instructors to complete the Tutorial.  All instructions are in the Repl.IT classroom for the Tutorial Questions for Week 03. Please submit your solutions using Repl.IT itself.

## Exercise 1 - Formatting

Modify the program to produce the output given below (don't print the first two lines and the blank line).
You have to use the following commands in the <iomanip> header file

  ```c++
#include <iostream>
using namespace std;
int main() {
   float marks[] = {78.4, 90.6, 45.9, 72.2, 54.4};
   char names[][20] = {"Ajith", "Wimal", "Kanthi", "Suranji", "Kushmitha"};
   cout << "No" << "Name" << "Marks" << endl;
   for (int r = 0; r < 5; r++) {
       cout <<  r+1 
            <<  names[r]
            << marks[r] << endl;
   }
}
```
```setw(), setprecision(), setiosflags(ios::fixed)```

Note : No has a width of 5, Name a width of 15, and Marks a width of 10, the marks are displayed with a precision of 2 decimal places.

```
0        1         2         3 
123456789012345678901234567890 


   No           Name     Marks
    1          Ajith     78.40
    2          Wimal     90.60
    3         Kanthi     45.90
    4        Suranji     72.20
    5      Kushmitha     54.40
```

 
## Exercise 2 – Functions with variables

Implement the method Volume() to compute the volume of a Box.

```int volume(int height, int width, int length)```

```c++
#include <iostream>
using namespace std;
int volume(int height, int width, int length);

int main() {
    int box1Height, box1Width, box1Length;
    int box2Height, box2Width, box2Length;
    int totalVolume, totalSurface;
    
    cout << "Enter Box 1 Height : ";
    cin >> box1Height;
    cout << "Enter Box 1 Width : ";
    cin >> box1Width;
    cout << "Enter Box 1 Length : ";
    cin >> box1Length;
    
     cout << "Enter Box 2 Height : ";
    cin >> box2Height;
    cout << "Enter Box 2 Width : ";
    cin >> box2Width;
    cout << "Enter Box 2 Length : ";
    cin >> box2Length;
    
    totalVolume = volume(box1Height, box1Width, box1Length)
             + volume(box2Height, box2Width, box2Length);
             
    cout << "Volume of Box is " << totalVolume << endl;
    
    return 0;
}

// Implement the Volume() function here
```
 
## Exercise 3 – Functions with structures

1. Create a structure to store the details of the Height, Width and Length called Box

use the struct command for this.
```
struct structname {
   datatype var1;
   datatype var2;
};
```

2. Create a variable of the structure type ```Box``` called ```box1```

3. Create a variable of the structure type ```Box``` called ```box2```

4. Input the height, width, length of box1 and box2

5. Replace the coding to pass box1 and box2 to the volume function

```c++
#include <iostream>

using namespace std;
int volume(int height, int width, int length);

// 1. Define a structure called Box
// have the integer data types Height, Width, Length

// Do not change the main function
int main() {
    // 2. Create a variable called box1 of the Box structure type
    // int box1Height, box1Width, box1Length;
    // 3. Create a variable called box2 of the Box structure type
    
    // int box2Height, box2Width, box2Length;
    int totalVolume;
    
    // 4. Input the height, width, lenght of box1 and box2
    cout << "Enter Box 1 Height : ";
    cin >> Height of Box 1;
    cout << "Enter Box 1 Width : ";
    cin >> Width of Box 1;
    cout << "Enter Box 1 Length : ";
    cin >> Length of Box 1;
    
    cout << "Enter Box 2 Height : ";
    cin >> Height of Box 2;
    cout << "Enter Box 2 Width : ";
    cin >> Width of Box 2;
    cout << "Enter Box 2 Length : ";
    cin >> Length of Box 2;
    
    // 5. Replace the coding below to pass the Box type structure
    totalVolume = volume( , , )
             + volume( , , );
    
    cout << "Volume of Box is " << totalVolume << endl;
    
    return 0;
}

// Implement the functions here
```

## Exercise 4 – Using Reference Type Parameters

Implement the Input function to input values for the parameters length and width from the keyboard.

1. Do you get the correct values printed ?

length and width passed as given below are really value type parameters. They do not return values from the function.

```void input(int length, int width);```

Reference type variables in C++ have a & sign in front of the parameter. Reference variables return values from the function.

2. Modify the parameters of your input function as given below, to use length and width as reference type parameters.

```void input(int &length, int &width);```

3. Do you get the correct values printed ?

```c++
#include <iostream>
using namespace std;

void print(int len, int wth);
void input(int len, int wth);

// Do not change the main() function
int main() {
   int length = 10, width = 5;
   input(length, width);
   print(length, width);
   return 0;
}

// Do not change the print() function
void print(int len, int wth) {
   cout << "Length : " << len 
        << ", Width  : " << wth << endl;
}

// Implement the Input Function here
```

