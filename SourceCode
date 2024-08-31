contacts = {}

def add_contact(name, phone, email=None):
        contacts[name] = {'phone': phone, 'email': email}
        print(f"Contact {name} added successfully.")

def update_contact(name, phone=None, email=None):
        if name in contacts:
            if phone:
                contacts[name]['phone'] = phone
            if email:
                contacts[name]['email'] = email
            print(f"Contact {name} updated successfully.")
        else:
            print(f"Contact {name} not found.")

def delete_contact(name):
        if name in contacts:
            del contacts[name]
            print(f"Contact {name} deleted successfully.")
        else:
            print(f"Contact {name} not found.")

def list_contacts():
        if contacts:
            for name, info in contacts.items():
                print(f"Name: {name}, Phone: {info['phone']}, Email: {info.get('email', 'N/A')}")
        else:
            print("No contacts found.")

def search_contact(search_term):
        found = False
        for name, info in contacts.items():
            if search_term in name or search_term in info.get('email', ''):
                print(f"Name: {name}, Phone: {info['phone']}, Email: {info.get('email', 'N/A')}")
                found = True
        if not found:
            print("No contacts found.")

def list_contacts_by_initial(initial):
        found = False
        for name in contacts:
            if name.startswith(initial):
                info = contacts[name]
                print(f"Name: {name}, Phone: {info['phone']}, Email: {info.get('email', 'N/A')}")
                found = True
        if not found:
            print(f"No contacts found starting with {initial}.")

while True:
        print("\nContact Management System")
        print("1. Add Contact")
        print("2. Update Contact")
        print("3. Delete Contact")
        print("4. List All Contacts")
        print("5. Search Contact")
        print("6. List Contacts by Initial Letter")
        print("7. Exit")
        choice = input("Enter your choice: ")

        if choice == '1':
            name = input("Enter name: ")
            phone = input("Enter phone number: ")
            email = input("Enter email (optional): ")
            add_contact(name, phone, email)
        elif choice == '2':
            name = input("Enter name: ")
            phone = input("Enter new phone number (leave blank to skip): ")
            email = input("Enter new email (leave blank to skip): ")
            update_contact(name, phone if phone else None, email if email else None)
        elif choice == '3':
            name = input("Enter name: ")
            delete_contact(name)
        elif choice == '4':
            list_contacts()
        elif choice == '5':
            search_term = input("Enter name or email to search: ")
            search_contact(search_term)
        elif choice == '6':
            initial = input("Enter initial letter: ")
            list_contacts_by_initial(initial)
        elif choice == '7':
            print("Exiting...")
            break
        else:
            print("Invalid choice. Please try again.")
