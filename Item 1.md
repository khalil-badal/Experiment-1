#Start

# Define a function to sort a string with numbers first, followed by letters
def sort_string_numbers_first(input_string):
    # Extract and sort all digits from the input string
    numbers = ''.join(sorted([char for char in input_string if char.isdigit()]))
    # Extract and sort all letters from the input string, case-insensitively
    letters = ''.join(sorted([char for char in input_string if char.isalpha()], key=str.lower))
    # Concatenate the sorted numbers and letters
    sorted_string = numbers + letters
    # Return the concatenated sorted string
    return sorted_string

# Define the main function to handle user input and output
def main():
    # Prompt the user to enter a string
    user_input = input("Enter a string: ")
    # Sort the input string with numbers first, followed by letters
    sorted_result = sort_string_numbers_first(user_input)
    # If the result is not empty and starts with a letter, capitalize the first letter
    if sorted_result and sorted_result[0].isalpha():
        sorted_result = sorted_result.capitalize()
    # Print the final arranged string
    print("Arranged string:", sorted_result)

# Check if the script is being run directly (not imported as a module)
if __name__ == "__main__":
    # Call the main function to execute the program
    main()

