# Difference-Arrays-ArrayLists

## Description
This project demonstrates the differences between Arrays and ArrayLists in Java. It includes examples of how to use both data structures, highlighting their respective advantages and limitations.

## Functions and Conceptual Differences

### Arrays
Arrays are a fundamental data structure in Java that store a fixed-size sequential collection of elements of the same type. Each element is accessed via an index.

- **Fixed Size:** The size is determined at creation and cannot be changed.
- **Type-Specific:** All elements must be of the same type.
- **Index-Based:** Access elements using their index, starting from 0.

### ArrayLists
ArrayLists are part of Java's Collection Framework and provide a more flexible, dynamically resizable array-like structure.

- **Dynamic Size:** Automatically resizes when elements are added or removed.
- **Type Safety with Generics:** Can store any type of objects, specified using generics.
- **Rich API:** Provides methods for manipulating the list, such as adding, removing, and searching elements.

## Code
The following Java code demonstrates the key differences between Arrays and ArrayLists:

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Demonstrating Arrays
        System.out.println("Array Example:");
        int[] intArray = new int[5]; // Fixed size array
        intArray[0] = 10;
        intArray[1] = 20;
        intArray[2] = 30;
        intArray[3] = 40;
        intArray[4] = 50;

        // Trying to add more elements would cause an ArrayIndexOutOfBoundsException
        // intArray[5] = 60; // This will cause an error

        for (int i : intArray) {
            System.out.println(i);
        }

        // Demonstrating ArrayList
        System.out.println("\nArrayList Example:");
        ArrayList<Integer> intArrayList = new ArrayList<>(); // Dynamic size ArrayList
        intArrayList.add(10);
        intArrayList.add(20);
        intArrayList.add(30);
        intArrayList.add(40);
        intArrayList.add(50);

        // ArrayList allows adding more elements without any issues
        intArrayList.add(60);

        for (int i : intArrayList) {
            System.out.println(i);
        }

        // Additional ArrayList functionalities
        System.out.println("\nArrayList contains 30: " + intArrayList.contains(30));
        intArrayList.remove(new Integer(30));
        System.out.println("ArrayList after removing 30: " + intArrayList);
    }
}
