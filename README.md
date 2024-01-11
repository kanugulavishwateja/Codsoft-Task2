def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Cannot divide by zero."

def calculator():
    print("Simple Calculator")

    while True:
        try:
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))
        except ValueError:
            print("Invalid input. Please enter valid numbers.")
            continue

        print("\nChoose Operation:")
        print("1. Addition (+)")
        print("2. Subtraction (-)")
        print("3. Multiplication (*)")
        print("4. Division (/)")

        operation = input("Enter the operation number (1-4): ")

        if operation in ('1', '2', '3', '4'):
            if operation == '1':
                result = add(num1, num2)
                print(f"\nResult: {num1} + {num2} = {result}")
            elif operation == '2':
                result = subtract(num1, num2)
                print(f"\nResult: {num1} - {num2} = {result}")
            elif operation == '3':
                result = multiply(num1, num2)
                print(f"\nResult: {num1} * {num2} = {result}")
            elif operation == '4':
                result = divide(num1, num2)
                print(f"\nResult: {num1} / {num2} = {result}")
            break
        else:
            print("Invalid operation. Please enter a number between 1 and 4.")

if __name__ == "__main__":
    calculator()
