print('Task#1')
from abc import ABC, abstractmethod

class Shape(ABC):
    def __init__(self, sides):
        self.sides = sides

    @abstractmethod
    def ComputeArea(self):
        pass


class Triangle(Shape):
    def __init__(self, base, height):
        super().__init__(3)
        self.base = base
        self.height = height

    def ComputeArea(self):
        return 0.5 * self.base * self.height


class Circle(Shape):
    def __init__(self, radius):
        super().__init__(0)
        self.radius = radius

    def ComputeArea(self):
        return 3.14159 * self.radius ** 2


def main():
    triangle = Triangle(4, 3)
    circle = Circle(5)

    print(f"Triangle Area: {triangle.ComputeArea()}")
    print(f"Circle Area: {circle.ComputeArea()}")


if __name__ == "__main__":
    main()





print("Task#2")
class Employee:
    def __init__(self, EmpName, EmpID, Salary):
        self.EmpName = EmpName
        self.EmpID = EmpID
        self.Salary = Salary

    def SalaryStatus(self):
        print(f"Employee Name: {self.EmpName}")
        print(f"Employee ID: {self.EmpID}")
        print(f"Salary: ${self.Salary}\n")


class BuildingManager(Employee):
    def __init__(self, EmpName, EmpID):
        super().__init__(EmpName, EmpID, 10000)


class ProcurementManager(Employee):
    def __init__(self, EmpName, EmpID):
        super().__init__(EmpName, EmpID, 12000)


class LogisticsManager(Employee):
    def __init__(self, EmpName, EmpID):
        super().__init__(EmpName, EmpID, 15000)


def main():
    employees = []

    building_manager = BuildingManager("Ibrahim Iftikhar", "261")
    procurement_manager = ProcurementManager("Ahmad", "772")
    logistics_manager = LogisticsManager("Ali", "153")

    employees.append(building_manager)
    employees.append(procurement_manager)
    employees.append(logistics_manager)

    for employee in employees:
        employee.SalaryStatus()


if __name__ == "__main__":
    main()
    
