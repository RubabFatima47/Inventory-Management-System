# Inventory-Management-System
# An inventory management system (or inventory system) is the process by which you track your goods throughout your entire supply chain, from purchasing to production to end sales. It governs how you approach inventory management for your business.

inventory = {}
def add_items(names,quantity,price):
    inventory[name] = {'quantity' : quantity,'price' : price }
    print("Added item: {name} ,quantity{quantity} ,price:  {price}")
    
def view_inventory(names,quantity,price):
    for names in inventory:
        inventory[name][quantity][price]
        
def update_inventory(names,change_in_quantity):
    if name in inventory:
        inventory[name]['quantity'] += change_in_quantity
        print(f"Updated 'name' {name} quantity to {inventory [name] ['quantity']}")
        view_inventory()
        
    else:
        print(f"{name} not included in inventory")

def del_item(name):
    if name in inventory:
        del inventory[name]
    else:
        print("item not found")
def main():
    add_items()
    view_inventory()
    update_inventory()
    del_item()
    
while True:
    print("1. Choose one option")
    print("2. Add item")
    print("3. View inventory")
    print("4. Update inventory")
    print("5. Delete item")
    print("6. Quit")
    choice = input("Enter")
    
    if choice == "1":
        name = input("Enter item name: ")
        quantity = int(input("Enter quantity: "))
        price = float(input("Enter price: "))
        add_items(name, quantity, price)
    elif choice == "2":
        view_inventory()
        
    elif choice == "3":
        name = input("Enter item name to update: ")
        change_in_quantity = int(input("Enter quantity change (e.g., +5 or -5): "))
        update_inventory(name, change_in_quantity)
        
    elif choice == "4":
        name = input("Enter item name to delete: ")
        del_item(name)
        
    elif choice == "5":
        print("Exiting program.")
        break
    else:
        print("Invalid choice. Please try again.")
    
if _name_ == '_main_':
    main()
