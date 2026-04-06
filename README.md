# simple-calculator
def calculate():
    print("\nSimple Calculator")
    print("Operations: +  -  *  /")

    try:
        num1 = float(input("Enter first number: "))
        operator = input("Enter operator: ")
        num2 = float(input("Enter second number: "))

        if operator == "+":
            print("Result:", num1 + num2)
        elif operator == "-":
            print("Result:", num1 - num2)
        elif operator == "*":
            print("Result:", num1 * num2)
        elif operator == "/":
            if num2 == 0:
                print("Error: Division by zero")
            else:
                print("Result:", num1 / num2)
        else:
            print("Invalid operator")

    except ValueError:
        print("Invalid input! Please enter numbers only.")

while True:
    calculate()
    again = input("\nDo you want to calculate again? (y/n): ").lower()
    if again != 'y':
        print("Goodbye 👋")
        break
