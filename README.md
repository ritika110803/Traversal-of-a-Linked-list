 C Program: Singly Linked List (Manual Creation & Traversal)

This project demonstrates how to create and traverse a *Singly Linked List* in C using dynamic memory allocation.

 Description

The program:

* Defines a struct Node for a linked list
* Allocates memory dynamically using malloc()
* Manually creates three nodes
* Links the nodes together
* Traverses the linked list
* Prints the elements

This example is ideal for beginners learning about *data structures* in C.

---

 Source Code

c

#include <stdio.h>

#include <stdlib.h>

// Define structure
struct Node {
    int data;
    struct Node* next;
};

int main() {
    // Creating nodes manually
    struct Node* head = NULL;
    struct Node* second = NULL;
    struct Node* third = NULL;

    // Allocate memory
    head = (struct Node*)malloc(sizeof(struct Node));
    second = (struct Node*)malloc(sizeof(struct Node));
    third = (struct Node*)malloc(sizeof(struct Node));

    // Assign data and link nodes
    head->data = 10;
    head->next = second;

    second->data = 20;
    second->next = third;

    third->data = 30;
    third->next = NULL;

    // Traversal
    struct Node* temp = head;
    printf("Linked List Elements: ");
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }

    return 0;
}


---

 How to Compile and Run

Using GCC

1. Save the file as linked_list.c
2. Open terminal or command prompt
3. Compile the program:


gcc linked_list.c -o linked_list


4. Run the executable:


./linked_list


(On Windows, use linked_list.exe)

---

Sample Output


Linked List Elements: 10 20 30


---

Concepts Covered

* Structures (struct) in C
* Pointers
* Dynamic memory allocation using malloc()
* Linked list creation
* Linked list traversal
* NULL pointer usage

---

How the Linked List Works

1. Memory is allocated for each node using malloc()
2. Each node contains:

   * data → stores the value
   * next → stores the address of the next node
3. The last node points to NULL
4. Traversal continues until NULL is reached

---

 ⚠️ Note

In a complete production program, you should also:

* Check if malloc() returns NULL
* Free allocated memory using free() to avoid memory leaks

---
