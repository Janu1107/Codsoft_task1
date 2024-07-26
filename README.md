# Codsoft_task1
Python code for To-Do-list
tasks = []

while True:
    print("\nChoose an option:")
    print("1. Add task")
    print("2. View tasks")
    print("3. Mark task as done")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == '1':
        task = input("Enter task description: ")
        tasks.append(task)
        print("Task added!")

    elif choice == '2':
        if not tasks:
            print("No tasks in the list!")
        else:
            for i, task in enumerate(tasks):
                print(f"{i+1}. {task}")

    elif choice == '3':
        if not tasks:
            print("No tasks in the list!")
        else:
            for i, task in enumerate(tasks):
                print(f"{i+1}. {task}")
            task_num = int(input("Enter task number to mark as done: ")) - 1
            if 0 <= task_num < len(tasks):
                del tasks[task_num]
                print("Task marked as done!")
            else:
                print("Invalid task number.")

    elif choice == '4':
        print("Exiting the To-Do List.")
        break

    else:
        print("Invalid choice. Please try again.")
