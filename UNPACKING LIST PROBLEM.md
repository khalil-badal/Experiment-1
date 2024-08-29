# UNPACKING LIST PROBLEM: Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

# Start

# Define a function named 'unpack_list' that takes one argument 'lst'
def unpack_list(lst):

    # Check if the length of the list is less than 3
    if len(lst) < 3:
        # If true, raise a ValueError with a message
        raise ValueError("List must contain at least three elements")

    # Assign the first element of the list to the variable 'first'
    first = lst[0]

    # Assign the last element of the list to the variable 'last'
    last = lst[-1]

    # Assign all elements between the first and last to the variable 'middle'
    middle = lst[1:-1]

    # Return the first, middle, and last elements as a tuple
    return first, middle, last

# Define the main function
def main():
    # Prompt the user to enter a list of numbers separated by commas and store it in 'user_input'
    user_input = input("Enter a list of numbers separated by commas: ")

    # Split the input string into individual numbers, convert them to integers, and store them in a list 'lst'
    lst = [int(num) for num in user_input.split(",")]

    # Check if the list has fewer than 3 elements
    if len(lst) < 3:
        # If true, print a message and exit the function
        print("Please enter a list with at least three elements.")
        return

    # Call the 'unpack_list' function with the list and unpack the returned tuple into 'first', 'middle', and 'last'
    first, middle, last = unpack_list(lst)

    # Print the first element
    print(f"First element: {first}")

    # Print the middle elements
    print(f"Middle elements: {middle}")

    # Print the last element
    print(f"Last element: {last}")

# Check if the script is being run directly
if __name__ == "__main__":
    # Call the 'main' function
    main()

# End 
