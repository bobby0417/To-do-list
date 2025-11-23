# To-do-list
tasks = []

def show_menu():
    print("
To-Do List App")
    print("1. View tasks")
    print("2. Add task")
    print("3. Update task")
    print("4. Delete task")
    print("5. Exit")

def view_tasks():
    if not tasks:
        print("No tasks found.")
    else:
        for i, task in enumerate(tasks, 1):
            print(f"{i}. {task}")

def add_task():
    task = input("Enter new task: ")
    tasks.append(task)
    print("Task added.")

def update_task():
    view_tasks()
    index = int(input("Enter task number to update: ")) - 1
    if 0 <= index < len(tasks):
        new_task = input("Enter updated task: ")
        tasks[index] = new_task
        print("Task updated.")
    else:
        print("Invalid task number.")

def delete_task():
    view_tasks()
    index = int(input("Enter task number to delete: ")) - 1
    if 0 <= index < len(tasks):
        tasks.pop(index)
        print("Task deleted.")
    else:
        print("Invalid task number.")

while True:
    show_menu()
    choice = input("Choose an option (1-5): ")
    if choice == "1":
        view_tasks()
    elif choice == "2":
        add_task()
    elif choice == "3":
        update_task()
    elif choice == "4":
        delete_task()
    elif choice == "5":
        print("Goodbye!")
        break
    else:
        print("Invalid choice. Please try again.")