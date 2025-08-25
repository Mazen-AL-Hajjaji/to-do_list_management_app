# To-Do List Management App

A simple and efficient command-line to-do list management application written in Python that allows you to create, view, complete, and delete tasks with persistent storage.

## Features

- **Task Management**: Create, view, and manage your daily tasks
- **Status Tracking**: Mark tasks as completed or pending
- **Persistent Storage**: Tasks are automatically saved to a JSON file
- **Interactive Menu**: Easy-to-use command-line interface
- **Input Validation**: Validates user input to prevent errors
- **Task Deletion**: Remove completed or unnecessary tasks
- **Status Toggle**: Switch tasks between completed and pending states

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
4. Padding Task
5. Delete Task
6. Exit

Enter your choice: 2
Enter the task description: Buy groceries

Task added.

 To-Do list Manager
1. View Tasks
2. Add Task
3. Complete Task
4. Padding Task
5. Delete Task
6. Exit

Enter your choice: 1

Your To-Do List: 
1. Buy groceries | [Pending]

 To-Do list Manager
1. View Tasks
2. Add Task
3. Complete Task
4. Padding Task
5. Delete Task
6. Exit

Enter your choice: 3

Your To-Do List: 
1. Buy groceries | [Pending]

Enter the task number to mark as complete: 1
Task marked as complete.
```

## How It Works

1. **Menu System**: Displays an interactive menu for user navigation
2. **Task Creation**: Collects task descriptions and stores them in memory
3. **Status Management**: Tracks completion status for each task
4. **Data Persistence**: Automatically saves tasks to a JSON file
5. **Input Validation**: Validates user input to prevent errors
6. **Task Operations**: Supports viewing, adding, completing, and deleting tasks

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

## File Structure

```
to-do_list_management_app/
├── main.py              # Main application file
├── todo_list.json       # Data storage file (created automatically)
└── README.md           # Documentation
```

## Error Handling

The program includes error handling for:
- Invalid menu selections
- Invalid task number inputs
- File I/O errors during save operations

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to submit issues, feature requests, or pull requests to improve this to-do list manager.

## Disclaimer

This to-do list manager is designed for personal and educational use. For professional task management needs, consider using established project management tools.
