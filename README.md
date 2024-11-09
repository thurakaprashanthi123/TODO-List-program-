todo_list = []

def add_task(task):
    todo_list.append({"task": task, "status": "pending"})

def remove_task(task_index):
    del todo_list[task_index]

def mark_complete(task_index):
    todo_list[task_index]["status"] = "completed"

def print_list():
    for index, task in enumerate(todo_list):
        print(f"{index+1}. {task['task']} ({task['status']})")

# Example usage:
add_task("Learn Python")
add_task("Build a web application")
add_task("Read a book")

print_list()

mark_complete(1)

print_list()
