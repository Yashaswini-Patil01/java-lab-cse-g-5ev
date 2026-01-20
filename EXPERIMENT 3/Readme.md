# EXPERIMENT-3
## 3a) Title: 
## Source Code:
```java
 class Student {
    String name;
    int age;
    double marks;

    Student() {
    }

    Student(String name, int age, double marks) {
        this.name = name;
        this.age = age;
        this.marks = marks;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
    }
}
class Main {
    public static void main(String[] args) {

        Student std = new Student();
        std.display();

        Student std1 = new Student("yashaswini", 19, 94.8);
        std1.display();

    }
}
```
## Output:
![output](d1.png)
