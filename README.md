┌───────────────────────────────────────────────────────────────────────────────┐
│                       STUDENT LOGIN & MANAGEMENT SYSTEM                        │
│                               (Advanced README)                                │
├───────────────────────────────────────────────────────────────────────────────┤

📘 PROJECT OVERVIEW
A role-based authentication and student management system developed in C. It 
supports Admin, Staff, and Guest functionalities with secure login, file-based 
storage, and CRUD operations on student records.

─────────────────────────────────────────────────────────────────────────────────

🔐 FEATURES

Secure Login & Authentication
• Password masking with '*'
• Reads credentials from credentials.txt
• Supports admin, staff, guest roles

Role-Based Menu Dispatcher
• Admin: Add, View, Search, Update, Delete
• Staff: Add, View, Search, Update
• Guest: View, Search only

Student Management
• Add new student
• Display all students
• Search student (case-insensitive)
• Update student using temp file
• Delete student safely via temp rewrite

File Handling
• credentials.txt → stores username/password/role
• students.txt → stores roll, name, marks
• Uses temp file mechanism to avoid data corruption

─────────────────────────────────────────────────────────────────────────────────

🏗 SYSTEM ARCHITECTURE

User → Login & Authentication → Role-Based Menu → Student Management  
           │                           │  
           │                           └────────→ Output / Reports  
           └────────→ credentials.txt                students.txt

─────────────────────────────────────────────────────────────────────────────────

📁 PROJECT STRUCTURE

Student-Login-System/
│── main.c
│── credentials.txt
│── students.txt
└── README.md

─────────────────────────────────────────────────────────────────────────────────

🖥 HOW TO RUN

Compile:
gcc main.c -o student_system

Run:
./student_system

─────────────────────────────────────────────────────────────────────────────────

📝 SAMPLE credentials.txt

admin admin123 admin
staff staff123 staff
guest guest123 guest

─────────────────────────────────────────────────────────────────────────────────

📝 SAMPLE students.txt

101 John 87.50
102 Alice 91.00
103 Bob 76.25

─────────────────────────────────────────────────────────────────────────────────

⚙ INTERNAL WORKING

• Login:
  - User enters username & password  
  - Password hidden with '*'  
  - Credentials verified from file

• CRUD Operations:
  - Add → append new record  
  - Display → read entire file  
  - Search → compare names ignoring case  
  - Update/Delete → rewrite via temp.txt  

─────────────────────────────────────────────────────────────────────────────────

🛡 SECURITY NOTES

• Password masking  
• Role-based operation restrictions  
• Temporary file method prevents corruption  
• No hardcoded credentials inside source code  

─────────────────────────────────────────────────────────────────────────────────

🌟 FUTURE ENHANCEMENTS

• Password encryption (SHA-256)  
• Replace text files with CSV/JSON/SQLite  
• Add sorting functionality  
• Implement GUI/Frontend  
• Create REST API backend  

─────────────────────────────────────────────────────────────────────────────────

🙌 CONTRIBUTING
Pull requests and improvements are welcome. For major changes, create an issue.

─────────────────────────────────────────────────────────────────────────────────

📜 LICENSE
MIT License – Open-source, free to modify and distribute.

└───────────────────────────────────────────────────────────────────────────────┘
