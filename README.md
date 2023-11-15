# Grocery-inventory-management
An inventory management system (or inventory system) is the process by which you track your goods throughout your entire supply chain, from purchasing to production to end sales. It governs how you approach inventory management for your business.
# Define a variable to store the inventory data as a dictionary
inventory = {}

# Define a function to add new items to the inventory
def add_items():
    # Ask the user how many items they want to add
    n = int(input("How many items do you want to add? "))
    # Use a for loop to iterate n times
    for i in range(n):
        # Ask the user the name and quantity of the item
        name = input("Enter the name of the item: ")
        quantity = int(input("Enter the quantity of the item: "))
        # Update the inventory with the item and quantity
        inventory.update({name: quantity})
        # Print a confirmation message
        print(f"Added {quantity} {name}(s) to the inventory.")

# Define a function to update existing items' quantities
def update_items():
    # Ask the user how many items they want to update
    n = int(input("How many items do you want to update? "))
    # Use a for loop to iterate n times
    for i in range(n):
        # Ask the user the name and quantity of the item
        name = input("Enter the name of the item: ")
        quantity = int(input("Enter the quantity to add or subtract: "))
        # Check if the item exists in the inventory
        if name in inventory:
            # Update the inventory with the new quantity
            inventory[name] += quantity
            # Print a confirmation message
            print(f"Updated {name} quantity to {inventory[name]}.")
        else:
            # Print an error message
            print(f"{name} does not exist in the inventory.")

# Define a function to view the current inventory
def view_items():
    # Print a header message
    print("The current inventory is:")
    # Use a for loop to iterate over the items and quantities in the inventory
    for item, quantity in inventory.items():
        # Print the item and quantity
        print(item, quantity)

# Define a function to remove items from the inventory
def remove_items():
    # Ask the user how many items they want to remove
    n = int(input("How many items do you want to remove? "))
    # Use a for loop to iterate n times
    for i in range(n):
        # Ask the user the name of the item
        name = input("Enter the name of the item: ")
        # Check if the item exists in the inventory
        if name in inventory:
            # Remove the item from the inventory and store the quantity
            quantity = inventory.pop(name)
            # Print a confirmation message
            print(f"Removed {quantity} {name}(s) from the inventory.")
        else:
            # Print an error message
            print(f"{name} does not exist in the inventory.")

# Define a function to display the menu options
def display_menu():
    # Print a welcome message
    print("Welcome to the Grocery Store Inventory Management Program.")
    # Print the menu options
    print("Please choose one of the following options:")
    print("1. Add new items to the inventory.")
    print("2. Update existing items' quantities.")
    print("3. View the current inventory.")
    print("4. Remove items from the inventory.")
    print("5. Exit the program.")

# Define a variable to store the user's choice
choice = 0

# Use a while loop to repeat until the user chooses to exit
while choice != 5:
    # Display the menu
    display_menu()
    # Ask the user to enter their choice
    choice = int(input("Enter your choice: "))
    # Use conditional statements to execute the corresponding function
    if choice == 1:
        # Call the add_items function
        add_items()
    elif choice == 2:
        # Call the update_items function
        update_items()
    elif choice == 3:
        # Call the view_items function
        view_items()
    elif choice == 4:
        # Call the remove_items function
        remove_items()
    elif choice == 5:
        # Print a farewell message
        print("Thank you for using the program. Goodbye.")
    else:
        # Print an invalid message
        print("Invalid choice. Please try again.")


 OUTPUT:       
Welcome to the Grocery Store Inventory Management Program.
Please choose one of the following options:
1. Add new items to the inventory.
2. Update existing items' quantities.
3. View the current inventory.
4. Remove items from the inventory.
5. Exit the program.
Enter your choice: 1
How many items do you want to add? 2
Enter the name of the item: milk
Enter the quantity of the item: 20
Added 20 milk(s) to the inventory.
Enter the name of the item: bread
Enter the quantity of the item: 15
Added 15 bread(s) to the inventory.
Please choose one of the following options:
1. Add new items to the inventory.
2. Update existing items' quantities.
3. View the current inventory.
4. Remove items from the inventory.
5. Exit the program.
Enter your choice: 3
The current inventory is:
milk 20
bread 15
Please choose one of the following options:
1. Add new items to the inventory.
2. Update existing items' quantities.
3. View the current inventory.
4. Remove items from the inventory.
5. Exit the program.
Enter your choice: 2
How many items do you want to update? 1
Enter the name of the item: milk
Enter the quantity to add or subtract: -5
Updated milk quantity to 15.
Please choose one of the following options:
1. Add new items to the inventory.
2. Update existing items' quantities.
3. View the current inventory.
4. Remove items from the inventory.
5. Exit the program.
Enter your choice: 4
How many items do you want to remove? 1
Enter the name of the item: bread
Removed 15 bread(s) from the inventory.
Please choose one of the following options:
1. Add new items to the inventory.
2. Update existing items' quantities.
3. View the current inventory.
4. Remove items from the inventory.
5. Exit the program.
Enter your choice: 5

