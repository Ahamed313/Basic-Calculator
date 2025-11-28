# Basic-Calculator

# Addition Function
def add(a, b):
    return a + b

# substruct Function
def subtract(a, b):
    return a - b

# multiply  Function
def multiply(a, b):
    return a * b

# division  Function
def divide(a, b):
    if b == 0:
        return "Cannot divide by zero"
    return a / b



def get_number(number):
    while True:
        try:
            value = float(input(number))
            return value
        except:
            print("Please enter a valid number.")



def basic_calculator():
    while True:
        print("\nBASIC CALCULATOR")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")

        choice = input("Enter your choice: ")

        if choice == "5":
            print("Exit Calculator")
            break

        num1 = get_number("Enter first number: ")
        num2 = get_number("Enter second number: ")

        if choice == "1":
            print(f"{num1} + {num2} = {add(num1, num2)}")
        elif choice == "2":
            print(f"{num1} - {num2} = {subtract(num1, num2)}")
        elif choice == "3":
            print(f"{num1} * {num2} = {multiply(num1, num2)}")
        elif choice == "4":
            result = divide(num2, num2)
            print(f"{num1} / {num2} = {result}")
        else:
            print("Invalid option.")




class Calculator:

    def add(self, a, b):
        return a + b
    
    def subtract(self, a, b):
        return a - b
    
    def multiply(self, a, b):
        return a * b
    
    def divide(self, a, b):
        if b == 0:
            return "Cannot divide by zero"
        return a / b

    def menu(self):
        print("\nCALCULATOR")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")

    def run(self):
        while True:
            self.menu()
            choice = input("Enter your choice: ")

            if choice == "5":
                print("Exit Calculator")
                break

            num1 = get_number("Enter first number: ")
            num2 = get_number("Enter second number: ")

            if choice == "1":
                print(f"{num1} + {num2} = {self.add(num1, num2)}")
            elif choice == "2":
                print(f"{num1} - {num2} = {self.subtract(num1, num2)}")
            elif choice == "3":
                print(f"{num1} * {num2} = {self.multiply(num1, num2)}")
            elif choice == "4":
                print(f"{num1} / {num2} = {self.divide(num1, num2)}")
            else:
                print("Invalid option! Please choose again.")


calc = Calculator()
calc.run()
