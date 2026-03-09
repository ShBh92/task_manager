**Task Manager with User Authentication (Python)**

**Overview**

This project is a command-line Task Manager application built using Python. It allows users to register, log in securely, and manage their personal tasks. Each user's tasks are stored separately, ensuring privacy and security.


**Features**

User Registration
Secure Login using Password Hashing
Add Tasks
View Tasks
Mark Tasks as Completed
Delete Tasks
Menu-driven command line interface
File-based persistent storage

**Technologies Used**

Python

**Project Structure**

task_manager/
├── task_manager.py
├── users.txt - created on first user registration
├── {username}_tasks.txt - automatically created based on registered user creating task. Deleted if all tasks are deleted for the respective user
└── README.md




**How It Works**
1. **Registration**
Users create a new account with a username and password. Passwords are hashed using SHA-256 before storing in users.txt.
2. **Login**
Users enter their credentials. The system verifies the hashed password and grants access if valid.
3. **Task Operations**
After login, users can:
View Tasks
Add Task
Mark Task as Completed
Delete Task
Logout
Each user has their own task file.

**Sample users.txt file data**

Test1,8a863b145dc6e4ed7ac41c08f7536c476ebac7509e028ed2b49f8bd5a3562b9f
Test2,32e6e1e134f9cc8f14b05925667c118d19244aebce442d6fecd2ac38cdc97649
Test3,68235f4551b9c6423df2af7ead63c90cdd4201ac08525bc3a41cd4755c6c86cb
Test4,b9cca56a720f2beee61f2e744ab3d20a95772a4315d18c5eee251a465f078012
Test5,f9ca438226aae2a1aa8503da8fe3aa57aca7036ca0ad8a2a381bec25e188c48b

**Sample username_tasks.txt file data**

0,Test5 Desc 1,Pending
1,Test5 Desc 2,Completed
3,Test5 Desc 4,Pending
