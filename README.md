# To-Do List Management App

A simple command-line to-do list management application written in Python that allows you to create, view, complete, and delete tasks with persistent storage in JSON format.

## Features

- **View Tasks**: Display all tasks with their completion status (Completed/Pending)
- **Add Tasks**: Create new tasks with custom descriptions
- **Mark Complete**: Mark tasks as completed
- **Mark Pending**: Mark completed tasks as pending again
- **Delete Tasks**: Remove tasks from the list
- **Persistent Storage**: Tasks are automatically saved to a JSON file
- **Input Validation**: Handles invalid inputs gracefully
- **Interactive Menu**: Easy-to-use command-line interface

## Requirements

- Python 3.x
- No external dependencies required (uses only built-in Python modules)

## Installation

1. Clone or download this repository
2. Navigate to the `to-do_list_management_app` directory
3. Run the script directly with Python

## Usage

Run the to-do list manager:

```bash
python main.py
```

The program will display a menu with the following options:

1. **View Tasks** - Display all current tasks with their status
2. **Add Task** - Create a new task with a description
3. **Complete Task** - Mark a task as completed
4. **Pending Task** - Mark a completed task as pending
5. **Delete Task** - Remove a task from the list
6. **Exit** - Close the application

### Example Session

```
 To-Do list Manager
1. View Tasks
2. Add Task
3. Complete Task
4. Pending Task
5. Delete Task
6. Exit

Enter your choice: 2
Enter the task description: Buy groceries

Task added.

 To-Do list Manager
1. View Tasks
2. Add Task
3. Complete Task
4. Pending Task
5. Delete Task
6. Exit

Enter your choice: 1

Your To-Do List: 
1. Buy groceries | [Pending]

 To-Do list Manager
1. View Tasks
2. Add Task
3. Complete Task
4. Pending Task
5. Delete Task
6. Exit

Enter your choice: 3

Your To-Do List: 
1. Buy groceries | [Pending]

Enter the task number to mark as complete: 1
Task marked as complete.
```

## How It Works

1. **Data Loading**: Attempts to load existing tasks from `todo_list.json`, creates empty list if file doesn't exist
2. **Menu Loop**: Displays interactive menu and processes user input
3. **Task Operations**: 
   - View: Shows numbered list with completion status
   - Add: Prompts for description, validates non-empty input
   - Complete/Pending: Shows task list, prompts for task number, validates input
   - Delete: Shows task list, prompts for task number, removes task
4. **Auto-Save**: All changes are automatically saved to JSON file
5. **Error Handling**: Validates inputs and provides helpful error messages

## Data Storage

Tasks are stored in `todo_list.json` with the following structure:

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

### File Creation

The `todo_list.json` file is created automatically when you add your first task. If you want to start with pre-existing tasks, you can create the file manually:

1. Create a new file named `todo_list.json` in the same directory as `main.py`
2. Add the following content:

```json
{
  "tasks": [
    {
      "description": "Your first task here",
      "complete": false
    },
    {
      "description": "Another task example",
      "complete": true
    }
  ]
}
```

**Note**: The `todo_list.json` file is not tracked by Git (it's in `.gitignore`), so each user will have their own personal task list.

## File Structure

```
to-do_list_management_app/
├── main.py              # Main application file
├── todo_list.json       # Data storage file (created when first task is added)
├── .gitignore          # Git ignore file
└── README.md           # Documentation
```

## Error Handling

The program includes comprehensive error handling:

- **File I/O Errors**: Gracefully handles missing or corrupted JSON files
- **Invalid Menu Choices**: Displays "Invalid choice. Please try again."
- **Invalid Task Numbers**: Validates task number input and shows "Invalid task number."
- **Non-Numeric Input**: Handles non-numeric inputs with "Please enter a valid number."
- **Empty Task Descriptions**: Prevents empty task descriptions with "Description cannot be empty"
- **Save Failures**: Shows "Failed to save" if file writing fails

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to submit issues, feature requests, or pull requests to improve this to-do list manager.

## Disclaimer

This to-do list manager is designed for personal and educational use. For professional task management needs, consider using established project management tools.
