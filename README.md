# To-do-list
todo_list = []

def show_menu():
    print("\n--- TO-DO LIST MENU ---")
    print("1. View tasks")
    print("2. Add task")
    print("3. Remove task")
    print("4. Exit")

while True:
    show_menu()
    choice = input("Enter your choice: ")

    if choice == '1':
        if not todo_list:
            print("No tasks yet.")
        else:
            for i, task in enumerate(todo_list, 1):
                print(f"{i
