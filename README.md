# ✅ Task 1: To-Do List

![Python](https://img.shields.io/badge/Python-3.6%2B-3776AB?logo=python&logoColor=white)
![Type](https://img.shields.io/badge/Type-Command--Line-blue)
![Storage](https://img.shields.io/badge/Storage-JSON-orange)

A menu-driven command-line application that helps you create, update and track your daily tasks. Tasks are saved to a file, so your list is still there the next time you open the program.

## 📌 Features

- ➕ **Add** a new task
- 📋 **View** all tasks with their status (`[ ]` pending, `[x]` done)
- ✏️ **Update** the title of an existing task
- ✔️ **Mark** a task as completed
- 🗑️ **Delete** a task
- 💾 **Auto-save** after every change to `tasks.json`
- 🛡️ Handles empty input, invalid task numbers and a missing or corrupted data file

## ▶️ How to Run

```bash
python task1_todo_list.py
```

No external libraries are required.

## 🖥️ Example Session

```
===== TO-DO LIST =====
1. View tasks
2. Add task
3. Update task
4. Mark task as done
5. Delete task
6. Exit

Choose an option (1-6): 2
Enter task: Buy milk
Task added.

Choose an option (1-6): 1

--- Your Tasks ---
1. [ ] Buy milk
```

## 🧠 How It Works

| Function | Purpose |
|----------|---------|
| `load_tasks()` | Reads `tasks.json` at startup; returns an empty list if the file is missing or invalid |
| `save_tasks(tasks)` | Writes the current list to `tasks.json` |
| `show_tasks(tasks)` | Prints the numbered list with completion marks |
| `get_index(tasks, prompt)` | Asks for a task number and validates it |
| `main()` | Runs the menu loop and calls the functions above |

### Data format

Each task is stored as a dictionary inside a JSON list:

```json
[
  { "title": "Buy milk", "done": false },
  { "title": "Study Python", "done": true }
]
```

## 📚 Concepts Used

Lists and dictionaries, `while` loops, functions, `try`/`except`, file I/O, the `json` and `os` modules.

## 🔮 Ideas for Improvement

- Due dates and priorities
- Sorting and filtering (pending / completed)
- A Tkinter GUI version
