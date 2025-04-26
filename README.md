# Week-4-python-


filename = input("Enter the filename to read: ")
try:
    with open(filename, 'r') as file:
        content = file.read()

   
    modified_content = content.upper()

    with open('modified_file.txt', 'w') as new_file:
        new_file.write(modified_content)

    print("File has been modified and saved as 'modified_file.txt'.")

except FileNotFoundError:
    print("Error: The file was not found.")
except IOError:
    print("Error: Could not read the file.")
