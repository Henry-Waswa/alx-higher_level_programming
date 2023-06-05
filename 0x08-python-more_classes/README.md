guillaume@ubuntu:~/0x08$ 
```
*No test cases needed**
### [7. Change representation](./7-rectangle.py)
* Write a class Rectangle that defines a rectangle by: (based on 6-rectangle.py)
*    Private instance attribute: width:
*        property **def width(self):** to retrieve it
*        property setter **def width(self, value):** to set it:
*            width must be an integer, otherwise raise a *TypeError* exception with the message *width must be an integer*
*            if width is less than 0, raise a *ValueError* exception with the message *width must be >= 0*
*    Private instance attribute: height:
*        property **def height(self):** to retrieve it
*        property setter **def height(self, value):** to set it:
*            height must be an integer, otherwise raise a *TypeError* exception with the message *height must be an integer*
*            if height is less than 0, raise a *ValueError* exception with the message *height must be >= 0*
*    Public class attribute number_of_instances:
*        Initialized to 0
*        Incremented during each new instance instantiation
*        Decremented during each instance deletion
*    Public class attribute print_symbol:
*        Initialized to #
*        Used as symbol for string representation
*        Can be any type
*    Instantiation with optional width and height: **def __init__(self, width=0, height=0):**
*    Public instance method: **def area(self):** that returns the rectangle area
*    Public instance method: **def perimeter(self):** that returns the rectangle perimeter:
*        if width or height is equal to 0, perimeter has to be equal to 0
*    **print()** and **str()** should print the rectangle with the character #:
*        if width or height is equal to 0, return an empty string
*    **repr()** should return a string representation of the rectangle to be able to recreate a new instance by using **eval()**
*    Print the message *Bye rectangle...* (... being 3 dots not ellipsis) when an instance of Rectangle is deleted
*    You are not allowed to import any module
```
guillaume@ubuntu:~/0x08$ cat 7-main.py
#!/usr/bin/python3
Rectangle = __import__('7-rectangle').Rectangle
my_rectangle_1 = Rectangle(8, 4)
print(my_rectangle_1)
print("--")
my_rectangle_1.print_symbol = "&"
print(my_rectangle_1)
print("--")
my_rectangle_2 = Rectangle(2, 1)
print(my_rectangle_2)
print("--")
Rectangle.print_symbol = "C"
print(my_rectangle_2)
print("--")
my_rectangle_3 = Rectangle(7, 3)
print(my_rectangle_3)
print("--")
my_rectangle_3.print_symbol = ["C", "is", "fun!"]
print(my_rectangle_3)
print("--")
guillaume@ubuntu:~/0x08$ ./7-main.py
########
########
########
########
--
&&&&&&&&
&&&&&&&&
&&&&&&&&
&&&&&&&&
--
##
--
CC
--
CCCCCCC
CCCCCCC
CCCCCCC
--
['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']
['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']
['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']['C', 'is', 'fun!']
--
Bye rectangle...
Bye rectangle...
Bye rectangle...
guillaume@ubuntu:~/0x08$ 
```
**No test cases needed**
### [8. Compare rectangles](./8-rectangle.py)
* Write a class Rectangle that defines a rectangle by: (based on 7-rectangle.py)
*    Private instance attribute: width:
*        property **def width(self):** to retrieve it
*        property setter **def width(self, value):** to set it:
*            width must be an integer, otherwise raise a *TypeError* exception with the message *width must be an integer*
*            if width is less than 0, raise a *ValueError* exception with the message *width must be >= 0*
*    Private instance attribute: height:
*        property **def height(self):** to retrieve it
*        property setter **def height(self, value):** to set it:
*            height must be an integer, otherwise raise a *TypeError* exception with the message *height must be an integer*
*            if height is less than 0, raise a *ValueError* exception with the message *height must be >= 0*
*    Public class attribute number_of_instances:
*        Initialized to 0
*        Incremented during each new instance instantiation
*        Decremented during each instance deletion
*    Public class attribute print_symbol:
*        Initialized to #
*        Used as symbol for string representation
*        Can be any type
*    Instantiation with optional width and height: **def __init__(self, width=0, height=0):**
*    Public instance method: **def area(self):** that returns the rectangle area
*    Public instance method: **def perimeter(self):** that returns the rectangle perimeter:
*        if width or height is equal to 0, perimeter has to be equal to 0
*    **print()** and **str()** should print the rectangle with the character #:
*        if width or height is equal to 0, return an empty string
*    **repr()** should return a string representation of the rectangle to be able to recreate a new instance by using **eval()**
*    Print the message *Bye rectangle...* (... being 3 dots not ellipsis) when an instance of Rectangle is deleted
*    Static method **def bigger_or_equal(rect_1, rect_2):* that returns the biggest rectangle based on the area
*        rect_1 must be an instance of Rectangle, otherwise raise a *TypeError* exception with the message *rect_1 must be an instance of Rectangle*
*        rect_2 must be an instance of Rectangle, otherwise raise a *TypeError* exception with the message *rect_2 must be an instance of Rectangle*
*        Returns rect_1 if both have the same area value
*    You are not allowed to import any module
```
guillaume@ubuntu:~/0x08$ cat 8-main.py
#!/usr/bin/python3
Rectangle = __import__('8-rectangle').Rectangle
my_rectangle_1 = Rectangle(8, 4)
my_rectangle_2 = Rectangle(2, 3)
if my_rectangle_1 is Rectangle.bigger_or_equal(my_rectangle_1, my_rectangle_2):
    print("my_rectangle_1 is bigger or equal to my_rectangle_2")
else:
    print("my_rectangle_2 is bigger than my_rectangle_1")
my_rectangle_2.width = 10
my_rectangle_2.height = 5
if my_rectangle_1 is Rectangle.bigger_or_equal(my_rectangle_1, my_rectangle_2):
    print("my_rectangle_1 is bigger or equal to my_rectangle_2")
else:
    print("my_rectangle_2 is bigger than my_rectangle_1")
guillaume@ubuntu:~/0x08$ ./8-main.py
my_rectangle_1 is bigger or equal to my_rectangle_2
my_rectangle_2 is bigger than my_rectangle_1
Bye rectangle...
Bye rectangle...
guillaume@ubuntu:~/0x08$ 
```
**No test cases needed**
### [9. A square is a rectangle](./9-rectangle.py)
* Write a class Rectangle that defines a rectangle by: (based on 8-rectangle.py)
*    Private instance attribute: width:
*        property **def width(self):** to retrieve it
*        property setter **def width(self, value):** to set it:
*            width must be an integer, otherwise raise a *TypeError* exception with the message *width must be an integer*
*            if width is less than 0, raise a *ValueError* exception with the message *width must be >= 0*
*    Private instance attribute: height:
*        property *def height(self):* to retrieve it
*        property setter **def height(self, value):** to set it:
*            height must be an integer, otherwise raise a *TypeError* exception with the message *height must be an integer*
*            if height is less than 0, raise a *ValueError* exception with the message *height must be >= 0*
*    Public class attribute number_of_instances:
*        Initialized to 0
*        Incremented during each new instance instantiation
*        Decremented during each instance deletion
*    Public class attribute print_symbol:
*        Initialized to #
*        Used as symbol for string representation
*        Can be any type
*    Instantiation with optional width and height: **def __init__(self, width=0, height=0):**
*    Public instance method: **def area(self):** that returns the rectangle area
*    Public instance method: **def perimeter(self):** that returns the rectangle perimeter:
*        if width or height is equal to 0, perimeter has to be equal to 0
*    **print()** and **str()** should print the rectangle with the character #:
*        if width or height is equal to 0, return an empty string
*    **repr()** should return a string representation of the rectangle to be able to recreate a new instance by using **eval()**
*    Print the message *Bye rectangle...* (... being 3 dots not ellipsis) when an instance of Rectangle is deleted
*    Static method **def bigger_or_equal(rect_1, rect_2):** that returns the biggest rectangle based on the area
        rect_1 must be an instance of Rectangle, otherwise raise a *TypeError* exception with the message *rect_1 must be an instance of Rectangle*
*        rect_2 must be an instance of Rectangle, otherwise raise a *TypeError* exception with the message *rect_2 must be an instance of Rectangle*
*        Returns rect_1 if both have the same area value
*    Class method **def square(cls, size=0):** that returns a new Rectangle instance with width == height == size
*    You are not allowed to import any module
```
guillaume@ubuntu:~/0x08$ cat 9-main.py
#!/usr/bin/python3
Rectangle = __import__('9-rectangle').Rectangle
my_square = Rectangle.square(5)
print("Area: {} - Perimeter: {}".format(my_square.area(), my_square.perimeter()))
print(my_square)
guillaume@ubuntu:~/0x08$ ./9-main.py
Area: 25 - Perimeter: 20
#####
#####
#####
#####
#####
Bye rectangle...
guillaume@ubuntu:~/0x08$ 
```
**No test cases needed**
### [11. N queens](./101-nqueens.py)
The N queens puzzle is the challenge of placing N non-attacking queens on an N×N chessboard. Write a program that solves the N queens problem.
*    Usage: nqueens N
*        If the user called the program with the wrong number of arguments, print Usage: nqueens N, followed by a new line, and exit with the status 1
*    where N must be an integer greater or equal to 4
*        If N is not an integer, print N must be a number, followed by a new line, and exit with the status 1
*        If N is smaller than 4, print N must be at least 4, followed by a new line, and exit with the status 1
*    The program should print every possible solution to the problem
*        One solution per line
*        Format: see example
*        You don’t have to print the solutions in a specific order
*    You are only allowed to import the sys module
Read: [Queen](https://en.wikipedia.org/wiki/Queen_%28chess%29), [Backtracking](https://en.wikipedia.org/wiki/Backtracking)
```
julien@ubuntu:~/0x08. N Queens$ ./101-nqueens.py 4
[[0, 1], [1, 3], [2, 0], [3, 2]]
[[0, 2], [1, 0], [2, 3], [3, 1]]
julien@ubuntu:~/0x08. N Queens$ ./101-nqueens.py 6
[[0, 1], [1, 3], [2, 5], [3, 0], [4, 2], [5, 4]]
[[0, 2], [1, 5], [2, 1], [3, 4], [4, 0], [5, 3]]
[[0, 3], [1, 0], [2, 4], [3, 1], [4, 5], [5, 2]]
[[0, 4], [1, 2], [2, 0], [3, 5], [4, 3], [5, 1]]
julien@ubuntu:~/0x08. N Queens$ 
```

---

## Author
* **Henry W. Waswa** - [Henry-Waswa](https://github.com/Henry-Waswa)
