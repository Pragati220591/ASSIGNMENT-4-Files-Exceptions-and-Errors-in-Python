# ASSIGNMENT-4-Files-Exceptions-and-Errors-in-Python
Module 5: Files, Exceptions, and Errors in Python
Task 1
filename = "sample.txt"
try:
    with open(filename, 'r') as file:
        for line in file:
            print(line.strip())
except FileNotFoundError:
    print(f"Error: The file '{filename}' does not exist.")

Task 2
data = input("Enter text to write to the file: ")

with open("output.txt", "w") as file:
    file.write(data + "\n")

with open("output.txt", "a") as file:
    append = input("Enter additional data to append: ")
    file.write(append + "\n")
    
print("\nFinal content of output.txt:")
with open("output.txt", "r") as file:
    print(file.read())
