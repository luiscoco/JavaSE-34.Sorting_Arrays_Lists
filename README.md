# JavaSE-Sorting Arrays Lists

Sorting arrays and lists in Java is a common task, and the language provides convenient ways to achieve this. Let's start with arrays.

## 1. Arrays.sort()

```java
import java.util.Arrays;

public class ArraySortingExample {
    public static void main(String[] args) {
        int[] numbers = {5, 2, 8, 1, 6};

        // Using Arrays.sort() for primitive types
        Arrays.sort(numbers);

        System.out.println("Sorted Array: " + Arrays.toString(numbers));
    }
}
```

In this example, Arrays.sort() is used to sort an array of integers in ascending order.

## 2. Sorting Objects(java.util.Arrays)

```java
import java.util.Arrays;

public class ObjectArraySortingExample {
    public static void main(String[] args) {
        // Custom class with Comparable interface implemented
        class Person implements Comparable<Person> {
            String name;
            int age;

            public Person(String name, int age) {
                this.name = name;
                this.age = age;
            }

            @Override
            public int compareTo(Person otherPerson) {
                // Compare persons based on age
                return Integer.compare(this.age, otherPerson.age);
            }

            @Override
            public String toString() {
                return name + " (" + age + " years old)";
            }
        }

        Person[] people = {
            new Person("Alice", 25),
            new Person("Bob", 30),
            new Person("Charlie", 22)
        };

        // Using Arrays.sort() for objects with Comparable interface
        Arrays.sort(people);

        System.out.println("Sorted People: " + Arrays.toString(people));
    }
}
```

Here, the Person class implements the Comparable interface, providing a way to compare and sort instances of the class.

## 3. Sorting Lists
For sorting lists, you can use the Collections.sort() method.

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class ListSortingExample {
    public static void main(String[] args) {
        List<Integer> numbers = new ArrayList<>();
        numbers.add(5);
        numbers.add(2);
        numbers.add(8);
        numbers.add(1);
        numbers.add(6);

        // Using Collections.sort() for lists
        Collections.sort(numbers);

        System.out.println("Sorted List: " + numbers);
    }
}
```

This example demonstrates sorting a list of integers using Collections.sort().



