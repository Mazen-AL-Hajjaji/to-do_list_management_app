# To-Do List Management App

A clean, efficient command-line to-do list application built in Python. Perfect for developers and anyone who prefers a simple, no-frills approach to task management.

## ✨ Features

- **Simple Task Management** - Add, view, complete, and delete tasks with ease
- **Status Tracking** - Clear visual indicators for completed and pending tasks
- **Persistent Storage** - Your tasks are automatically saved to a JSON file
- **Input Validation** - Robust error handling for a smooth user experience
- **Cross-Platform** - Works on Windows, macOS, and Linux
- **No Dependencies** - Uses only Python's built-in libraries

## 🚀 Quick Start

### Prerequisites
- Python 3.x (any recent version)

### Installation
```bash
# Clone the repository
git clone https://github.com/Mazen-AL-Hajjaji/to-do_list_management_app.git

# Navigate to the project directory
cd to-do_list_management_app

# Run the application
python main.py
```

## 📖 Usage

The app provides an intuitive command-line interface with these options:

| Option | Description |
|--------|-------------|
| **1** | View all tasks with their current status |
| **2** | Add a new task to your list |
| **3** | Mark a task as completed |
| **4** | Mark a completed task as pending |
| **5** | Delete a task from your list |
| **6** | Exit the application |

### Example Workflow

```
 To-Do list Manager
1. View Tasks
2. Add Task
3. Complete Task
4. Pending Task
5. Delete Task
6. Exit

Enter your choice: 2
Enter the task description: Complete project documentation

Task added.

Enter your choice: 1

Your To-Do List: 
1. Complete project documentation | [Pending]
```

## 💾 Data Storage

Tasks are stored locally in `todo_list.json` with this structure:

```json
{
  "tasks": [
    {
      "description": "Your task description",
      "complete": false
    }
  ]
}
```

### File Management
- The JSON file is created automatically when you add your first task
- You can manually create the file with pre-existing tasks if desired

## 🛠️ How It Works

1. **Load Data** - Reads existing tasks from `todo_list.json` or starts with an empty list
2. **Display Menu** - Shows available options in a clean interface
3. **Process Input** - Validates user input and performs requested operations
4. **Auto-Save** - All changes are immediately saved to the JSON file
5. **Error Handling** - Graceful handling of invalid inputs and file operations

## 🔧 Error Handling

The application includes comprehensive error handling:

- **Missing Files** - Creates new file if `todo_list.json` doesn't exist
- **Invalid Input** - Validates menu choices and task numbers
- **Empty Descriptions** - Prevents creation of tasks without descriptions
- **File I/O Errors** - Handles save failures gracefully
- **User Feedback** - Clear error messages guide users to correct input

## 📁 Project Structure

```
to-do_list_management_app/
├── main.py              # Main application
├── todo_list.json       # User data (created automatically)
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Report bugs or suggest features
- Submit pull requests
- Improve documentation
- Add new functionality

## 📄 License

This project is open source and available under the MIT License.

## ⚠️ Disclaimer

This application is designed for personal and educational use. For enterprise or critical task management needs, consider using established project management tools.
