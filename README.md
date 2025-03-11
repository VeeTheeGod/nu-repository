#python 3.7.1

print ("My Calculator")
def calculate(num1, num2, operator):
    """
    Performs a mathematical operation on two numbers.

    Args:
        num1: The first number.
        num2: The second number.
        operator: The mathematical operator (+, -, *, /).

    Returns:
        The result of the operation or an error message.
    """
    if operator == '+':
        return num1 + num2
    elif operator == '-':
        return num1 - num2
    elif operator == '*':
        return num1 * num2
    elif operator == '/':
        if num2 == 0:
            return "Error: Division by zero"
        else:
            return num1 / num2
    else:
        return "Error: Invalid operator"

def main():
    """
    Gets user input, performs calculation, and prints the result.
    """
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operator = input("Enter the operator (+, -, *, /): ")

        result = calculate(num1, num2, operator)
        print(f"{num1} {operator} {num2} = {result}")

    except ValueError:
        print("Error: Invalid number input.")

if __name__ == "__main__":
    main()
