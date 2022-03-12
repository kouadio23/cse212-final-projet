**Data Structure Tutorial**

**I-Welcome**

**Introduction**

Welcome to my Python Fundamentals Tutorial. Python is a  powerful programming language. It’s a great first language because it is concise and easy to read.There are three very important basic topics every beginning Python programmer should understand:
- [Queue](2-queue.md)
- [Set](3-set.md)
- [Tree](4-tree.md)

**Contact**

For questions or comments, please send them to:

Kouadio kouao, BYU-Idaho, CSE 212

kouaokouadio@gmail.com



**II-Queue**

1. Definition (Enqueue/Dequeue)

In Data structure, a queue consists of a list of records such that records are added at one end and removed from the other. It follows the FIST-IN-FIST-OUT (FIFO) principle. In other word enqueuing (first-in) and dequeuing (first-out). 
 

* Enqueue

Enqueuing, is adding an element to the end of the queue. Lets assume we are in a line at a counter. the first person to enter the line will definately be the one at the begining of the line no matter how long the line gets.

Lets look at the following piagram:

<img src="pic1.png" alt="Enqueue diagram">

In this diagram, we are enqueueing the red box to the rest of the boxes. So it will be added to at the end of the line.

* Implementing 

Lets consider a queue of persons in a line:

\#lets enqueue some persons into the list

```
person = []
person.append('Frank')
person.append('Mark')
person.append('Ella')
person.append('Emerauld')
print(person) 

#result: ['Frank','Mark','Ella','Emerauld']

```
Here we use the "append" operation of the list to simulate the core operations of a queue.


* Dequeue

Dequeuing, is removing an element at the beggining of the queue. With our previous example, we are in a line at a counter. the first person to enter the line will be the first to be taking care of at the counter, therfore the first to exit the queue.

Lets look at the following piagram:

<img src="pic2.png" alt="Dequeue diagram">

In this diagram, we are dequeueing a box from the rest of the boxes. So the first one in the line; The green box  will be separated from the rest of the boxes.

* Implementing 

Lets consider the presious queue of persons in a line:

```
#lets enqueue some persons into the list 

person = []
person.append('Frank')
person.append('Mark')
person.append('Ella')
person.append('Emerauld')

#Now lets dequeue a person from the list

first_person = person.pop(0)
print(first_person) 

#result: ['Frank']

```
Here we use the "pop" operation of the list to simulate the core operations of a queue.

* Performance

Accessing a specific element of the Queue can be done in linear time O(n), as we need to traverse it. But we usually have a pointer/reference to the first and last element of the queue. Therefore both enqueue and dequeue can be performed in constant time O(1).

*  [Problem](queue-problem.py)

Try the problem first before looking at the solution

* [Solution](queue-solution.py)


**III-Set**

1. Definition 

A set is a data structure that can store any number of unique values in any order. Sets are different from arrays in the sense that they only allow non-repeated, unique values within them.

2. Implementing 

Lets see deferrence between an array and a set:


```
>>> an_array = [1,2,2,3,3,4] # repeated values
>>> a_set = set(an_array) # non-repeated, unique values
>>> a_set
{1, 2, 3, 4}

```
In this example, we can see that the numbers in the array can be repeated while they cannot in the set.

This can also be used for strings:

```
>>> a_string = "my name is Fulgence Dalo"
>>> a_set = set(a_string)
>>> a_set
{'m', ' ', 'y', 'n', 'a', 'i', 's', 'F', 'u', 'l', 'g', 'e', 'c', 'D', 'o'}
```
Here we can see that when implementing the set, the letters are not repeatred.

We can use the "add(value)" to add a value to a set and "remove(value)" to remove a value from a set.

* Performance



*  [Problem](set-problem.py)

Try the problem first before looking at the solution

* [Solution](set-solution.py)




**IV-TREE**

1. Definition 

A tree is a non linear data structure as opposed to stack, linked list and queues. As the name indicates, tree needs to have at most 2 elements called binary tree. Since each element in a binary tree can have only 2 children, we typically name them the left and right child. 
Each node contains three components:

Pointer to left subtree
Pointer to right subtree
Data element
 

2. Types of tree

* Full binary tree

It is a tree in which every node in the tree has either 0 or 2 children.
<img src="rooted-binary.webp">


* Perfect binary tree

 It is a binary tree in which all interior nodes have two children and all leaves have the same depth or same level.
 <img src="perfect-binary.webp">

* complete binary tree

It is a binary tree in which every level, except possibly the last, is completely filled, and all nodes are as far left as possible.
<img src="complete.webp">

* Balanced binary tree

A binary tree is height balanced if the left and right subtrees' heights differ by at most one, AND
The left subtree is balanced, AND
The right subtree is balanced.
An empty tree is height balanced. This produces an o(logn) performance.
<img src="balanced.webp">

* Degenerated binary tree

It is a tree is where each parent node has only one child node. It behaves like a linked list. This produces a O(n) performance because it is not balabed.
<img src="degenarated.webp">

3. Implementing 

* Binary search tree

```
# Function to search a given key in BST

def search(root, key):

    # Base Cases: root is null or key is present at root
    if root is None or root.val == key:
        return root

    # Key is greater than root's key
    if root.val < key:
        return search(root.right, key)

    # Key is smaller than root's key
    return search(root.left, key)

```

* Insert in a BST

when inserting data in a tree, the greater values are added to the right while the smaller to the left.



*  [Problem](queue-problem.py)

Try the problem first before looking at the solution

* [Solution](queue-solution.py)
