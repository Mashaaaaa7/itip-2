# itip-2

Emloyee.java
public abstract class Employee {

    private String name;
    private int age;

    public Employee (String name, int age) {
        this.name = name;
        this.age = age;
    }

    public Employee (String name, String age) {
        this("Мария", 20);
    }

    public String getName() {

  
        return name;
    }

    public void setName(String name) {
        this.name=name; // Устанавливаем новое значение для имени
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public abstract void displayInfo(); // Абстрактный метод, который должен быть реализован в подклассах

    public String toString() {
        return "Имя: " + name + ", Возраст: " + age;
    }

}




Main.java


public class Main {
    public static void main(String[] args) {
        Programmist Programmist1 = new Programmist ("Максим", 21,25000,"Java");
        Administrator Administrator1 = new Administrator("Мария", 20, 25000, 2);
        Manager Manager1 = new Manager("Илья", 21, 25000,3);


        Programmist1.displayInfo();
        Administrator1.displayInfo();
        Manager1.displayInfo();
    }
}



Programmist.java
public class Programmist extends Employee {

    private String name; // имя
    private int age; //возраст
    private double salary; // зарплата
    private String programmingLanguage; //язык программирования

    public Programmist(String name, int age, double salary, String programmingLanguage) {
        super(name, age); //аргументы name, age
        this.salary = salary;
        this.programmingLanguage = programmingLanguage;
    }

    public Programmist() {
        this("Максим", 20, 25000, null);
    }
    // Геттеры и сеттеры
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public String getProgrammingLanguage() {
        return programmingLanguage;
    }

    public void setProgrammingLanguage(String programmingLanguage) {
        this.programmingLanguage = programmingLanguage;
    }

    @Override

    public String toString() {
        return "Программист: " + "Максим" + ", возраст:" + 21 + ", заработанная плата: " + salary + ", язык программирования: " + programmingLanguage;
    }

    public void displayInfo() {
        System.out.println("Программист:" + "Максим" + ", возраст:" + 21 + ", Зарплата: " + salary + ", язык программирования: " + programmingLanguage);
    }
}



Administrator.java
public class Administrator extends Employee {

    private String name; // имя
    private int age; //возраст
    private double salary; // зарплата
    private int yearsOfExperience; // опыт работы

    public Administrator(String name, int age, double salary, int yearsOfExperience) {
        super(name, age);
        this.salary = salary;
        this.yearsOfExperience = yearsOfExperience;
    }

    public Administrator() {
        this("Мария", 20, 25000, 2);
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public int getYearsOfExperience() {
        return yearsOfExperience;
    }

    public void setYearsOfExperience(int yearsOfExperience) {
        this.yearsOfExperience = yearsOfExperience;
    }


    @Override

    public String toString() {
        return "Администратор: " + "Мария" + ", возраст:" + 20 + ", Зарплата: " + getSalary() + ", Опыт работы: " + getYearsOfExperience() + " лет";
    }

    public void displayInfo() {
        System.out.println("Администратор: " + "Мария" + ", возраст:" + 20 + ", Зарплата: " + getSalary() + ", Опыт работы: " + getYearsOfExperience() + " лет");
    }
}

Manager.java
public class Manager extends Employee {

    private String name; // имя
    private int age; //возраст
    private double salary; // зарплата
    private int yearsOfExperience; // опыт работы (int вместо String)

    public Manager(String name, int age, double salary, int yearsOfExperience) {
        super(name, age);
        this.salary = salary;
        this.yearsOfExperience = yearsOfExperience;
    }

    public Manager() {
        this("Илья", 21, 25000, 3); // Передайте значения в конструктор с параметрами
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public int getYearsOfExperience() {
        return yearsOfExperience;
    }

    public void setYearsOfExperience(int yearsOfExperience) {
        this.yearsOfExperience = yearsOfExperience;
    }

    @Override
    public String toString() {
        return "Менеджер: " + "Илья" + ", возраст:" + 21 + ", Зарплата: " + getSalary() + ", Опыт работы: " + getYearsOfExperience() + " лет";
    }

    public void displayInfo() {
        System.out.println("Менеджер: " + "Илья" + ", возраст:" + 21 + ", Зарплата: " + getSalary() + ", Опыт работы: " + getYearsOfExperience() + " лет");
    }
}
