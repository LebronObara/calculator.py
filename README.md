# calculator.py

def calculate(num1, num2, operation):
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        if num2 != 0:
            return num1 / num2
        else:
            return "Error: Division by zero is not allowed."
    else:
        return "Error: Invalid operation."

def main():
    print("Welcome to the Basic Calculator!")
    
    # Input: Get two numbers and an operation from the user
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (+, -, *, /): ")

        # Perform the calculation
        result = calculate(num1, num2, operation)

        # Output: Display the result
        if isinstance(result, str):
            print(result)  # Print error message if any
        else:
            print(f"{num1} {operation} {num2} = {result}")

    except ValueError:
        print("Error: Please enter valid numbers.")
        if __name__ == "__main__":
    main()
