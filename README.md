# Simple Calculator with User Permission

def calculator():
    while True:
        print("\n--- Calculator Menu ---")
        print("1. Addition")
        print("2. Subtraction")
        print("3. Multiplication")
        print("4. Division")

        try:
            choice = int(input("Enter your choice (1-4): "))
            if choice not in [1, 2, 3, 4]:
                print("Invalid choice! Try again.")
                continue

            a = float(input("Enter first number: "))
            b = float(input("Enter second number: "))

            if choice == 1:
                print("Result =", a + b)
            elif choice == 2:
                print("Result =", a - b)
            elif choice == 3:
                print("Result =", a * b)
            elif choice == 4:
                if b == 0:
                    print("Error! Division by zero is not allowed.")
                else:
                    print("Result =", a / b)

        except ValueError:
            print("Invalid input! Please enter numbers only.")

        # Permission to continue
        permission = input("\nDo you want to continue? (yes/no): ").lower()
        if permission != "yes":
            print("Calculator closed. Thank you!")
            break


# Main permission
start = input("Do you want to start the calculator? (yes/no): ").lower()
if start == "yes":
    calculator()
else:
    print("Permission denied. Program ended.")
# Calculater
