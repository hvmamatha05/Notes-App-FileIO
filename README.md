
# Task 4: Java File I/O – Notes App

## Objective
A text-based notes manager that reads and writes notes to a file using Java File I/O.

## Tools Used
- Java
- Notepad
- Terminal / Command Prompt

## Concepts Covered
- FileWriter (write/append to file)
- FileReader + BufferedReader (read from file)
- try-with-resources (auto-closes streams)
- IOException handling
- Checked vs Unchecked exceptions
- Append mode vs Overwrite mode

## How to Run
```
javac NotesApp.java
java NotesApp
```

## Features
- Add a note (appends to notes.txt)
- View all saved notes (reads line by line)
- Clear all notes (overwrites with empty content)
- Menu-driven loop

## Project Structure
```
NotesApp.java
  └── class NotesApp
        ├── addNote()   → FileWriter (append=true) + BufferedWriter
        ├── viewNotes() → FileReader + BufferedReader
        └── clearNotes() → FileWriter (append=false)

notes.txt → auto-created when first note is added
```

## Sample Output
```
--- Notes Manager ---
1. Add Note
2. View Notes
3. Clear All Notes
4. Exit
Enter choice: 1
Enter your note: Buy groceries tomorrow
Note saved.

Enter choice: 2
--- Your Notes ---
1. Buy groceries tomorrow
```

## Append vs Overwrite
| Mode | Code | Effect |
|------|------|--------|
| Append | `new FileWriter(file, true)` | Adds to existing content |
| Overwrite | `new FileWriter(file, false)` | Replaces all content |

## Key Learnings
- How FileWriter and FileReader work internally
- Why BufferedReader is preferred over FileReader alone (faster, line-by-line reading)
- How try-with-resources automatically closes file streams
- How to handle IOException properly
- Difference between checked and unchecked exceptions
