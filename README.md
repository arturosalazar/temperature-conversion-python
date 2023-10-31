# Temperature Conversion Program

This Python program includes two primary functions: convertToFahrenheit and convertToCelsius. These functions allow for the conversion of temperatures between Celsius and Fahrenheit.

## Exercise Description:
    The convertToFahrenheit function takes a temperature in degrees Celsius as a parameter and returns the temperature converted to degrees Fahrenheit. Conversely, the convertToCelsius function takes a temperature in degrees Fahrenheit and returns the temperature in degrees Celsius.

The program makes use of the following formulas for temperature conversion:

    Fahrenheit to Celsius: Celsius = (Fahrenheit - 32) × (5 / 9)
    Celsius to Fahrenheit: Fahrenheit = Celsius × (9 / 5) + 32

The provided assert statements are used to validate the correctness of the conversion functions. They act as test cases and will raise an AssertionError if the conditions are not met, ensuring that the functions are returning accurate conversions.

## How to run the program:
    Prerequisites: Ensure you have Python installed on your machine.
    Navigate: Open a terminal or command prompt and navigate to the directory containing the program file
    Run: Execute the program using the command: python temp-conversion.py.
    Make sure to replace python with python3 if your system defaults to Python 2.

## Example Usage:
You can call the functions directly with a temperature value to convert. Here is an example of how they work:

    celsius_temp = convertToCelsius(32)
    print(f"32 degrees Fahrenheit is {celsius_temp} degrees Celsius.")

    fahrenheit_temp = convertToFahrenheit(0)
    print(f"0 degrees Celsius is {fahrenheit_temp} degrees Fahrenheit.")
    
## Testing
The program includes assert statements that serve as unit tests to ensure the correctness of the conversion functions:

    assert convertToCelsius(0) == -17.77777777777778
    assert convertToCelsius(180) == 82.22222222222223
    assert convertToFahrenheit(0) == 32
    assert convertToFahrenheit(100) == 212
    assert convertToCelsius(convertToFahrenheit(15)) == 15
    # Rounding errors cause a slight discrepancy:
    assert convertToCelsius(convertToFahrenheit(42)) == 42.00000000000001

Your program is working correctly if it does not raise any AssertionError when run.

## Note on Rounding Errors

Due to the floating-point arithmetic and the way Python handles floating-point numbers, there might be a slight discrepancy in some of the assert conditions due to rounding errors. This is normal and expected behavior.