# Automating Allow List Updates in Python

This project is part of my Cybersecurity portfolio and was developed during the **Google Cybersecurity Professional Certificate** course.

In this activity, I take on the role of a security professional responsible for helping keep the environment secure, investigating possible security threats, and ensuring system access controls are properly maintained.

## The Scenario

At my organization, access to restricted content is controlled with an allow list of IP addresses identified in the `"allow_list.txt"` file. A separate remove list identifies IP addresses that should no longer have access to this content.

My mission was to create an algorithm to automate updating the `"allow_list.txt"` file and remove these IP addresses that should no longer have access.

## Tools and Technologies Explored

* **Language:** Python.
* **File Operations:** Use of the `.open()` function in read (`"r"`) and write (`"w"`) modes, managed via `with` statements.
* **Data Manipulation Methods:** Application of `.read()`, `.split()`, `.remove()`, and `.join()` methods.
* **Control Flow:** Use of `for` loops and conditional `if` statements.

---

## The Investigation and Adjustments

I utilized Python programming and string/list manipulation techniques to execute the following steps:

1. **Opening the allow list file:** Assigned the file name to the `import_file` variable and opened the `"allow_list.txt"` file using a `with` statement alongside the `.open()` function in read mode.
2. **Reading file contents:** Applied the `.read()` method to convert the imported file into a string stored in the variable `ip_addresses`.
3. **Converting the string into a list:** Used the `.split()` method to convert the `ip_addresses` string into a list format, splitting by whitespace so individual IP addresses could be easily managed.
4. **Iterating through the remove list:** Incorporated a `for` loop to cycle through each IP address element contained within the `remove_list`.
5. **Removing matching IP addresses:** Created a conditional statement to evaluate if the loop variable was in `ip_addresses`, then applied the `.remove()` method to eliminate matching entries safely.
6. **Reformatting the list into a string:** Used the `.join()` method with newline separators (`"\n"`) to convert the list of `ip_addresses` back into a single string format.
7. **Rewriting and updating the file:** Used a second `with` statement with open in write mode (`"w"`) and the `.write()` method to overwrite the contents of `"allow_list.txt"` with the revised list.

## My Conclusion

This activity reinforced how programming and automation are fundamental for administrative workflows and access control management. The ability to process, filter, and update files programmatically allows for maintaining clean and accurate security lists.

**Key improvements implemented:**
* Automation of the IP address review and removal process.
* Accurate conversion and manipulation of file data between strings and lists.
* Optimization of data filtering through conditional checks before element removal.

> **What I learned from this:** I deepened my knowledge of Python file handling, iteration logic, and data structure manipulation. I understood in practice how using functions and methods like `.open()`, `.read()`, `.split()`, `.remove()`, `.join()`, and `.write()` allows raw file data to be transformed into clean, updated security configurations.

---
*Feel free to explore the project details and the utilized commands available in this repository!*
