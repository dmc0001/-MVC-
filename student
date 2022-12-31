// The Model

public class Student {
  private String name;
  private int age;

  public Student(String name, int age) {
    this.name = name;
    this.age = age;
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
}

// The View

import javax.swing.*;

public class StudentView {
  public void printStudentDetails(String studentName, int studentAge) {
    System.out.println("Student: ");
    System.out.println("Name: " + studentName);
    System.out.println("Age: " + studentAge);
  }
}

// The Controller

public class StudentController {
  private Student model;
  private StudentView view;

  public StudentController(Student model, StudentView view) {
    this.model = model;
    this.view = view;
  }

  public void setStudentName(String name) {
    model.setName(name);
  }

  public String getStudentName() {
    return model.getName();
  }

  public void setStudentAge(int age) {
    model.setAge(age);
  }

  public int getStudentAge() {
    return model.getAge();
  }

  public void updateView() {
    view.printStudentDetails(model.getName(), model.getAge());
  }
}

// The Test Drive

public class MVCTestDrive {
  public static void main(String[] args) {
    // fetch student record based on his roll no from the database
    Student model  = retriveStudentFromDatabase();

    // Create a view : to write student details on console
    StudentView view = new StudentView();

    StudentController controller = new StudentController(model, view);

    controller.updateView();

    // update model data
    controller.setStudentName("John");

    controller.updateView();
  }

  private static Student retriveStudentFromDatabase(){
    Student student = new Student("Robert", 0);
    return student;
  }
}
