# JAVA-OOPS
Daily coding practice and OOP concepts in C++ and Java

#COPY-CONSTRUCTOR
package oops;

public class copyConstructor {
    public static class Student {
        int age;
        int roll_no;
        String name;

        Student(String n, int a, int r) {
            name = n;
            age = a;
            roll_no = r;


        }
        Student(Student obj){
            name = obj.name;
            age = obj.age;
            roll_no = obj.roll_no;
        }
        void display(){
            System.out.println(name);
            System.out.println(age);
            System.out.println(roll_no);
        }
    }

    public static void main(String[] args) {
        Student s1 = new Student("Danish",21,108);
        Student s2 = new Student(s1);
        s2.display();
    }
}

*****************************************************************************************************************************************
#FUNCTION OVERLOADING

package oops;

public class functionOverloading {
    static class Addition{
        int add(int a, int b){
            return a+b;
        }
        int add(int a , int b, int c){
            return a+b+c;
        }
        double add(double a, double b){
            return a+b;
        }

        public static void main(String[] args) {
            Addition obj = new Addition();
            System.out.println(obj.add(10,20));
            System.out.println(obj.add(10,20,30));
            System.out.println(obj.add(5.5,5.8));
        }
    }

}

*************************************************************************************************************************************************
#OPERATOR OVERLOADING 

package oops;

public class OperatorOverLoadding {
    static class Test {
        public static void main(String[] args) {
            int a = 10;
            int b = 20;
            System.out.println(a + b);
        }
    }
}

***************************************************************************************************************************************************
#POLYMORPHISM

package oops;

public class polymorphism {
    public static class Dog {
        void speak() {
            System.out.println("nn");
        }
    }

        public static class Cat {
            void speak() {
                System.out.println("tt");
            }

            public static class Human {
                void speak() {
                    System.out.println("Hello");
                }

            }


            public static void main(String[] args) {
                Dog d = new Dog();
                Cat c = new Cat();
                Human h = new Human();

                d.speak();
                c.speak();
                h.speak();

            }
        }
    }

*******************************************************************************************************************************************
#USER DEFINE DATATYPES

package oops;

public class userdefinedatatypes {
    public static class Student {
        String name;
        int rno;
        double cgpa ;

    }

    public static void main(String[] args) {
        Student s1 = new Student();
        s1.name="dan";
        s1.rno=2353;
        s1.cgpa=7.8;

        Student s2 = new Student();
        s2.name="gg";
        s2.rno=2354;
        s2.cgpa=6.8;

        Student s3 = new Student();
        s3.name="tt";
        s3.rno=2355;
        s3.cgpa=5.8;

        System.out.println(s1.name+" "+s1.rno+" "+s1.cgpa);

    }
}

*****************************************************************************************************************************************
#PASSING CLASSES TO THE METHOD

package oops;

public class passingClassestoMethod {
    public static class Car{
        int seat;
        String name;
        double length;
        String type;
        void print (){
            System.out.println(seat+" "+name+" "+length+" "+type);
        }
    }

    public static void main(String[] args) {
        Car c = new Car ();
        c.length = 3.99;
        c.name = "Ks";
        c.seat = 4;
        c.type = "SUV";
        change(c);
        System.out.println(c.seat);
        c.print();


    }
    public static void change(Car c){
        c.seat = 5;
    }
    }

************************************************************************************************************************************************
#MULTIPLE INHERITANCE
package oops;

public class Multiple {
    interface A {
        void show();
    }

    interface B {
        void display();
    }

    static class Test implements A, B {

        @Override
        public void show() {
            System.out.println("Show method");
        }

        @Override
        public void display() {
            System.out.println("Display method");
        }
    }

    public static void main(String[] args) {
        Test t = new Test();
        t.show();
        t.display();
    }
}



