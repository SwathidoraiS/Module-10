# Queue-Queue Values in Descending Order Using Python 🧮

This Python program simulates a queue using a list, removes the first two elements (FIFO order), and displays the remaining values in descending order.

## 🎯 Aim

To write a Python program to:
- Accept user inputs into a list (queue)
- Remove the first two elements (simulating dequeue)
- Display the remaining values in **descending order**

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` to determine how many elements will be added.
3. Loop `n` times:
   - Read an input value.
   - Append it to the list `q`.
4. Remove the first element using `pop(0)`.
5. Remove the second element using `pop(0)` again.
6. Sort the list in descending order.
7. Print the updated list.

## 🧪 Program: 
~~~c
queue = []
n = int(input("Enter the number of elements in the queue: "))
for i in range(n):
    value = int(input(f"Enter element {i + 1}: "))
    queue.append(value)
if len(queue) >= 2:
    queue.pop(0)
    queue.pop(0)
elif len(queue) == 1:
    queue.pop(0)
    print("Only one element was in the queue, so it's now empty.")
else:
    print("The queue is empty. Nothing to remove.")
if queue:
    queue.sort(reverse=True)
    print("Remaining elements in descending order:", queue)
else:
    print("No elements remaining in the queue.")
~~~

### Output:
![Screenshot 2025-05-11 155148](https://github.com/user-attachments/assets/7f245c84-d125-4356-a0e0-7c1301bde878)


## Result:
Thus the program has been executed successfully.

# Queue-Remove Two String Values from the Rear End in Python 🧵

This Python program demonstrates how to manage a list of strings and remove the last two elements (i.e., from the rear of the list).

## 🎯 Aim

To write a Python program to:
- Accept `n` string values from the user
- Remove the last two values (rear end of the list)
- Display the updated list

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` from the user (number of strings).
3. Loop `n` times:
   - Read a string input.
   - Append it to the list `q`.
4. Remove the last element using `pop()`.
5. Remove the next last element using `pop()` again.
6. Display the updated list.

##  Program:
~~~c
string_list = []
n = int(input("Enter the number of strings: "))
for i in range(n):
    val = input(f"Enter string {i + 1}: ")
    string_list.append(val)
if len(string_list) >= 2:
    string_list.pop()
    string_list.pop()
elif len(string_list) == 1:
    string_list.pop()
    print("Only one string was in the list, so it's now empty.")
else:
    print("The list is empty. Nothing to remove.")
if string_list:
    print("Updated list after removing last two elements:", string_list)
else:
    print("No elements remaining in the list.")
~~~

### Output:
![Screenshot 2025-05-11 155507](https://github.com/user-attachments/assets/e3b0d5a6-8fcc-4773-b780-b3d248ba565a)


## Result:
Thus the program has been executed successfully.

# Stack Implementation Using `LifoQueue` (Max Size 7) 🔄

This Python program demonstrates a stack implemented using the `LifoQueue` class from the `queue` module. It allows up to 7 elements, checks if the stack is full, and then prints the elements in reverse (LIFO) order.

## 🎯 Aim

To create a Python program that:
- Implements a stack using `LifoQueue` with a maximum size of 7
- Adds user-inputted values to the stack
- Checks whether the stack is full
- Prints the stack elements in reverse order (LIFO)

## 📋 Algorithm

1. Import the `LifoQueue` class from the `queue` module.
2. Create a stack with a maximum size of 7.
3. Read the number of elements (`n`) to be added to the stack.
4. Loop `n` times:
   - Read a value from the user.
   - Use `put()` to push it onto the stack if it's not full.
5. Use `full()` to check if the stack is full and print the result.
6. Use `get()` repeatedly to pop and print elements in reverse order.

## Program
~~~c
from queue import LifoQueue
stack = LifoQueue(maxsize=7)
print("Enter up to 7 elements to push onto the stack:")
for i in range(7):
    value = input(f"Enter value {i + 1} (or press Enter to stop): ")
    if value == "":
        break
    stack.put(value)
if stack.full():
    print("The stack is full.")
else:
    print(f"The stack is not full. Current size: {stack.qsize()}")
print("\nStack elements in LIFO order:")
while not stack.empty():
    print(stack.get())
~~~

## 🧪 Sample Input and Output
![Screenshot 2025-05-11 155805](https://github.com/user-attachments/assets/44f17f4e-c9c0-4720-89ad-8f3acdc03737)


## Result:
Thus the program has been executed successfully.

# # Stack-Stack Reversal Program 🔁

This Python program demonstrates how to reverse the values in a stack using basic stack operations like push and pop.

## 🎯 Aim

To write a Python program that reverses the values in a stack using standard stack operations.

## 📋 Algorithm

1. Create an empty stack.
2. Read an integer `n` from the user (number of elements to push).
3. Loop `n` times:
   - Read an integer from the user.
   - Push it onto the stack.
4. Create an empty list called `reverse`.
5. While the stack is not empty:
   - Pop the top element.
   - Append it to `reverse`.
6. Print the reversed list.


### Program:
~~~c
def reverse_stack(stack):
    reversed_stack = []
    while stack:
        reversed_stack.append(stack.pop())
    return reversed_stack
stack = []
n = int(input("Enter the number of elements in the stack: "))
for i in range(n):
    value = input(f"Enter element {i + 1}: ")
    stack.append(value) 
print("\nOriginal Stack (Top to Bottom):")
print(stack[::-1]) 
stack = reverse_stack(stack)
print("\nReversed Stack (Top to Bottom):")
print(stack[::-1])
~~~

## 🧪 Sample Input and Output
![Screenshot 2025-05-11 160130](https://github.com/user-attachments/assets/72d011b8-d294-46b1-a15a-85581aee471d)


## Result
Thus the program has been executed successfully.

# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
~~~c
class CircularQueue:
    def __init__(self, size):
        self.queue = [None] * size
        self.size = size
        self.front = self.rear = -1

    def enqueue(self, value):
        if (self.rear + 1) % self.size == self.front:
            print("Queue is full!")
            return
        if self.front == -1:
            self.front = self.rear = 0
        else:
            self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = value
    def dequeue(self):
        if self.front == -1:
            print("Queue is empty!")
            return None
        removed = self.queue[self.front]
        if self.front == self.rear:
            self.front = self.rear = -1
        else:
            self.front = (self.front + 1) % self.size
        return removed
cq = CircularQueue(3)
print("Enter 3 values for the Circular Queue:")
for i in range(3):
    val = input(f"Enter value {i + 1}: ")
    cq.enqueue(val)
removed_values = []
for _ in range(3):
    removed = cq.dequeue()
    if removed is not None:
        removed_values.append(removed)
print("\nRemoved values from the Circular Queue:")
print(removed_values)
~~~

### Output:
![Screenshot 2025-05-11 160445](https://github.com/user-attachments/assets/b9300e73-e6f1-4a9b-9299-5d83085177e4)

## Result:
Thus the program has been executed successfully.
