def get_user_input():
    try:
        weight = float(input("Enter your weight in kilograms: "))
        height = float(input("Enter your height in meters: "))
        if weight <= 0 or height <= 0:
            print("Weight and height must be positive numbers.")
            return None, None
        return weight, height
    except ValueError:
        print("Invalid input. Please enter numeric values.")
        return None, None

def calculate_bmi(weight, height):
    if height == 0:
        return None  
    return weight / (height ** 2)

def interpret_bmi(bmi):
    if bmi < 18.5:
        return "Underweight"
    elif 18.5 <= bmi < 24.9:
        return "Normal weight"
    elif 25 <= bmi < 29.9:
        return "Overweight"
    else:
        return "OBESE"

def main():
    while True:
        
        weight, height = get_user_input()
        if weight is None or height is None:
            continue

      
        bmi = calculate_bmi(weight, height)
        if bmi is None:  
            print("Invalid height. Please try again.")
            continue

        
        category = interpret_bmi(bmi)

      
        print(f"Your BMI is {bmi:.2f}, which falls under the category: {category}")

        again = input("Do you want to calculate again? (yes/no): ").strip().lower()
        if again != "yes":
            break


main()
