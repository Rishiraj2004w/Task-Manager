# Task-Manager
A Task Manager oversees project tasks, assigns responsibilities, tracks progress, and ensures deadlines are met efficiently. They coordinate team efforts, optimize workflows, and resolve bottlenecks to improve productivity.
!!CODE IS HERE!!


def task():
    tasks = []  # Empty list
    print("Welcome to Task Management APP------")

    total_tasks = int(input("Enter how many tasks you want to add = "))  # User input for number of tasks

    for i in range(total_tasks):  # Looping through all tasks
        task_name = input(f"Enter task {i + 1} = ")  # Enter task 
        tasks.append(task_name)

    print(f"Today's tasks are: {tasks}")

    while True:
        operation = int(input("\nEnter operation:\n1 - Add\n2 - Update\n3 - Delete\n4 - View\n5 - Exit\nChoice: "))

        if operation == 1:
            add = input("Enter task you want to add = ")
            tasks.append(add)
            print(f"Task '{add}' has been successfully added...")

        elif operation == 2:
            update_val = input("Enter task you want to update = ")
            if update_val in tasks:
                up = input("Enter new task = ")
                ind = tasks.index(update_val)
                tasks[ind] = up
                print(f"Task '{update_val}' has been successfully updated to '{up}'")
            else:
                print("Task not found!")

        elif operation == 3:
            delete_val = input("Enter task you want to delete = ")
            if delete_val in tasks:
                tasks.remove(delete_val)
                print(f"Task '{delete_val}' has been successfully deleted...")
            else:
                print("Task not found!")

        elif operation == 4:
            print(f"Total tasks = {tasks}")

        elif operation == 5:
            print("Closing the program...")
            break

        else:
            print("Invalid operation! Please enter a valid choice (1-5).")

# Calling the function to execute
task()
