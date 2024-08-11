# py
def add_task(tasks):
  task = input("Enter the task: ")
  tasks.append(task)
  print(f"Task '{task}' added to the list.")

def view_tasks(tasks):
  if not tasks:
    print("To-do list is empty.")
  else:
    print("To-Do List:")
    for index, task in enumerate(tasks, start=1):
      print(f"{index}. {task}")

def remove_task(tasks):
  view_tasks(tasks)
  try:
    index = int(input("Enter the task number to remove: "))
    if 1 <= index <= len(tasks):
      removed_task = tasks.pop(index - 1)
      print(f"Task '{removed_task}' removed.")
    else:
      print("Invalid task number.")
  except ValueError:
    print("Invalid input. Please enter a number.")

def main():
  tasks = []
  while True:
    print("\nTo-Do List App")
    print("1. Add task")
    print("2. View tasks")
    print("3. Remove task")
    print("4. Quit")
    choice = input("Enter your choice: ")

    if choice == '1':
      add_task(tasks)
    elif choice == '2':
      view_tasks(tasks)
    elif choice == '3':
      remove_task(tasks)
    elif choice == '4':
      break
    else:
      print("Invalid choice. Please try again.")

if _name_ == "_main_":
  main()
