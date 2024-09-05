# Todo App

This is a simple **Todo App** built using **React** that allows users to add, edit, complete, and delete tasks. It showcases state management using `useState` and context through a custom `TodoContext`.

## Features

- **Add Todo:** Add a new task to the todo list.
- **Edit Todo:** Edit existing tasks (if they are not completed).
- **Mark Complete:** Toggle the completion status of a task using a checkbox.
- **Delete Todo:** Remove tasks from the list permanently.

## Technologies Used

- **React**: A JavaScript library for building user interfaces.
- **Context API**: Used for state management across components.
- **Tailwind CSS**: For styling the app with utility-first CSS.

## Installation and Setup Instructions

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/your-username/todo-app.git
    ```

2. Navigate to the project directory:
    ```bash
    cd todo-app
    ```

3. Install the dependencies:
    ```bash
    npm install
    ```

4. Start the development server:
    ```bash
    npm start
    ```

   The app should now be running on [http://localhost:3000](http://localhost:3000).

## Usage

1. **Add Todo:** Type a task in the input box and click the "Add" button or press "Enter".
2. **Edit Todo:** Click the edit button (✏️) next to a task, modify the task text, and click the save button (📁).
3. **Mark Complete:** Check the checkbox to mark a task as completed.
4. **Delete Todo:** Click the delete button (❌) to remove a task.

## Components

### `TodoForm.js`
This component renders the input form for adding a new todo. It uses the `useState` hook to manage the form input and triggers the `addTodo` function from `TodoContext` to add the todo to the list.

### `TodoItem.js`
Each todo is rendered as a `TodoItem`. The component allows users to:
- Toggle the completion status of the task.
- Edit the task if it's not marked complete.
- Delete the task using the delete button.

It leverages `useState` to manage the editable state of each todo and interacts with context functions like `updateTodo`, `toggleComplete`, and `deleteTodo`.

## Context (`TodoContext.js`)

The `TodoContext` provides the following functions:
- **addTodo**: Adds a new todo.
- **updateTodo**: Updates an existing todo.
- **toggleComplete**: Toggles the completion status of a todo.
- **deleteTodo**: Deletes a todo from the list.

This context makes it easier to share state and methods between components without having to pass props down multiple levels.