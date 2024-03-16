# improved-fiesta
Fiesta Car Rentals--
--User can look up available inventory of vechile by color and type
--User can then rent the vechile choosen
--User can then return the vechile
--User can see updated inventory anytime(rented/returned)

Contributors:
Chelsea Rhea: username-Chelsea Rhea
Benjamin Hogan: username-BenRHogan
Ling Jin: username-lingjin0725





Pseudocode final project: 

 

class Vehicle: 

    ////////////////////# Vehicle class representing a vehicle with type, color, and availability attributes 

    attributes: type, color, available 

////////////////class to determine the starting point of all vehicles available  

type(trucks, cars, vans) 

color(red, blue, black) 

 

red trucks # available 

blue trucks # available 

black trucks # available 

 

red cars # available 

blue cars # available 

black cars # available 

 

red vans # available 

blue vans # available 

black vans # available 

 

 

/////////////class InventoryManagementSystem: 

    # InventoryManagementSystem class to manage the inventory of vehicles 

    //////////////////attributes: inventory 

 

    method __init__(): 

        # Constructor to initialize an empty inventory list 

        initialize empty inventory list 

 

    method add_vehicle(vehicle): 

        # Method to add a vehicle to the inventory list 

        add vehicle to inventory list 

 

    method view_inventory(): 

        # Method to display the inventory 

        display inventory 

 

    method rent_vehicle(type, color): 

        # Method to rent a vehicle of a specific type and color 

        search for vehicle matching type and color 

        if found: 

            if vehicle.available: 

                # If the vehicle is available, decrement its availability and return success message 

                decrement vehicle availability 

                return success message 

            else: 

                # If the vehicle is not available, return failure message 

                return failure message 

        else: 

            # If the vehicle is not found, return vehicle not found message 

            return vehicle not found message 

 

    method return_vehicle(type, color): 

        # Method to return a rented vehicle of a specific type and color 

        search for vehicle matching type and color 

        if found: 

            # If the vehicle is found, increment its availability and return success message 

            increment vehicle availability 

            return success message 

        else: 

            # If the vehicle is not found, return vehicle not found message 

            return vehicle not found message 

 

////////////////////////class Menu: /////////////////////

/////////////////////////    # Menu class to display menu options and get user choice (main class) //////////////

Menu  

View inventory 

Rent 

Return 

Exit 

Menu will loop until user exits/ will be easy to add GUI to the main menu loop 

    method display_menu(): 

        # Method to display menu options 

        display menu options 

 

    method get_user_choice(): 

        # Method to get user choice from input 

        get user choice from input 

 

def main(): 

    # Main function to run the program 

    create inventory management system 

    create menu 

 

    loop until user chooses to exit: 

        # Loop until user chooses to exit 

        display menu 

        get user choice 

 

        if choice == 1: 

            # If user chooses to view inventory, call view_inventory method 

            inventory_system.view_inventory() 

        elif choice == 2: 

            # If user chooses to rent a vehicle, get vehicle type and color, and call rent_vehicle method 

            type = input("Enter vehicle type: ") 

            color = input("Enter vehicle color: ") 

            message = inventory_system.rent_vehicle(type, color) 

            print(message) 

        elif choice == 3: 

            # If user chooses to return a vehicle, get vehicle type and color, and call return_vehicle method 

            type = input("Enter vehicle type: ") 

            color = input("Enter vehicle color: ") 

            message = inventory_system.return_vehicle(type, color) 

            print(message) 

        elif choice == 4: 

            # If user chooses to exit, exit the program 

            exit program 

        else: 

            # If user enters an invalid choice, display error message 

            print("Invalid choice, please try again") 

 

if __name__ == "__main__": 

    # Run the main function when the script is executed 

    main() 
