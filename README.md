# Temperature Converter 🌡️  

## Overview  
This is **Day 2** of my **30-Day Python Coding Challenge**! This simple yet effective Temperature Converter lets users **convert Celsius to Fahrenheit** and vice versa through an interactive menu.  

## Features  
✅ Convert **Celsius to Fahrenheit** and **Fahrenheit to Celsius**  
✅ Interactive menu with a **loop** for multiple conversions  
✅ **Error handling** for invalid inputs  

## Code  
```python
def celsius_to_fahrenheit(celsius):
    return (celsius * 9 / 5) + 32

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5 / 9

print("🌡️ Welcome to the Temperature Converter! 🌡️")
while True:
    print("\nMenu:")
    print("1. Convert Celsius to Fahrenheit")
    print("2. Convert Fahrenheit to Celsius")
    print("3. Exit")
    choice = input("Enter your choice (1, 2, or 3): ").strip()
    
    if choice == '1':
        try:
            celsius = float(input("Enter temperature in Celsius: "))
            print(f"{celsius}°C is equivalent to {celsius_to_fahrenheit(celsius):.2f}°F\n")
        except ValueError:
            print("Invalid input! Please enter a numerical value.\n")
    elif choice == '2':
        try:
            fahrenheit = float(input("Enter temperature in Fahrenheit: "))
            print(f"{fahrenheit}°F is equivalent to {fahrenheit_to_celsius(fahrenheit):.2f}°C\n")
        except ValueError:
            print("Invalid input! Please enter a numerical value.\n")
    elif choice == '3':
        print("Thank you for using the Temperature Converter. Goodbye!")
        break
    else:
        print("Invalid choice! Please select option 1, 2, or 3.\n")
