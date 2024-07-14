"""
To-do List application
A command-line to-do list application that allows users to add, remove, and view tasks.
"""
import sys

# This list is main source where all data will be stored
Todo_list = []


# This is main function that will run all function
def main():
    choose_the_option()
    view()
    remove()
    add()


def choose_the_option():
    # This function asked what action user want to do
    # and depending on that action program make action
    print("To-do List Application")
    while True:
        print("\t\t\t---------------------\n"
              "\t\t\t1) view tasks\n"
              "\t\t\t2) remove tasks\n"
              "\t\t\t3) add tasks\n"
              "\t\t\t4) quit\n"
              "\t\t\t--------------------")

        try:
            option = int(input("Waiting for input: "))
            if option == 1:
                view()
            elif option == 2:
                remove()
            elif option == 3:
                add()
            elif option == 4:
                sys.exit()
        except ValueError:
            print("Invalid input. Please enter a number (1-4).")

def view():
    # This function will output to-do list and go back to choose_the_option()
    # this variable to check if there's something in list
    number_of_task = len(Todo_list)
    if number_of_task == 0:
        print("\nThere's no tasks.")
        print("You have to add some new or quit the program.\n")
    else:
        for index, task in enumerate(Todo_list, start=1):
            print(f"{index}) {task}")


def remove():
    # Half program is alike to view().
    # Program asks if there is element in list and if this True then
    # This functino output Todo_list and then asking what task user want to remove and remove task

    number_of_task = len(Todo_list)
    if number_of_task == 0:
        print("\nThere's no tasks.")
        print("You have to add some new or quit the program.\n")
    else:
        for index, task in enumerate(Todo_list, start=1):
            print(f"{index}) {task}")
        try:
            which_task_to_remove = int(input("Which one of the task you want to remove?(enter element): "))
            if 1 <= which_task_to_remove <= number_of_task:
                removed_task = Todo_list.pop(which_task_to_remove - 1)
                print(f"Removed task: {removed_task}\n")
            else:
                print("Invalid task number.\n")
        except ValueError:
            print("Invalid input. Please enter a number.\n")


def add():
    # This function is made for adding elements into list
    which_task_to_add = input("What task do you want to add? ")
    Todo_list.append(which_task_to_add)
    while True:
        another_one = input("Add another one(\"-\" sign to stop): ")
        if another_one != "-":
            Todo_list.append(another_one)
        else:
            break


main()
