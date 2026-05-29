# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
~~~
class Details:
    
    def getName(self):
        self.name = input("Enter Name: ")
    
    def getAge(self):
        self.age = int(input("Enter Age: "))

class Employee(Details):
    
    def getEmployeeDetails(self):
        print("\n--- Employee Details ---")
        self.getName()
        self.getAge()
        self.employee_id = input("Enter Employee ID: ")
        self.department = input("Enter Department: ")
        
    def displayEmployee(self):
        print("\nEmployee Information")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)

class Patient(Details):
    
    def getPatientDetails(self):
        print("\n--- Patient Details ---")
        self.getName()
        self.getAge()
        self.patient_id = input("Enter Patient ID: ")
        self.disease = input("Enter Disease: ")
        
    def displayPatient(self):
        print("\nPatient Information")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)

e = Employee()
e.getEmployeeDetails()
e.displayEmployee()

p = Patient()
p.getPatientDetails()
p.displayPatient()
~~~
## Sample Output
~~~
--- Employee Details ---
Enter Name: Arun
Enter Age: 30
Enter Employee ID: E101
Enter Department: IT

Employee Information
Name: Arun
Age: 30
Employee ID: E101
Department: IT

--- Patient Details ---
Enter Name: Ramesh
Enter Age: 45
Enter Patient ID: P205
Enter Disease: Fever

Patient Information
Name: Ramesh
Age: 45
Patient ID: P205
Disease: Fever
~~~
