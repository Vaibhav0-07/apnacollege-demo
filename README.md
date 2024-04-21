# apnacollege-demo
this is my first repo 


#include <iostream>
#include <vector>
#include <string>

using namespace std;

// Define a class for Employee
class Employee {
public:
    string name;
    double salary;

    Employee(string n, double s) : name(n), salary(s) {}
};

// Define a class for PayrollSystem
class PayrollSystem {
private:
    vector<Employee> employees;

public:
    void addEmployee(string name, double salary) {
        employees.push_back(Employee(name, salary));
    }

    void calculatePayroll() {
        cout << "Payroll Information:" << endl;
        for (const auto& emp : employees) {
            cout << "Employee: " << emp.name << ", Salary: $" << emp.salary << endl;
        }
    }
};

int main() {
    PayrollSystem payroll;

    // Adding employees
    payroll.addEmployee("John", 3000.0);
    payroll.addEmployee("Alice", 3500.0);
    payroll.addEmployee("Bob", 3200.0);

    // Calculating and displaying payroll
    payroll.calculatePayroll();

    return 0;
}
