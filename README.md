# To-Do List Application Documentation with Vue.js and Tailwind CSS

## Application Description
This to-do list application allows users to add, complete, and delete tasks. Each task can have a user-defined date and time. The app uses Vue.js for reactivity and Tailwind CSS for styling. Task data is stored in `localStorage` to ensure data persistence.

## Key Features
- **Add Task**: Users can add new tasks by entering task text and (optionally) selecting a date and time.
- **Mark Task as Complete**: Users can mark tasks as completed, which will display the task text with a strikethrough.
- **Delete Task**: Users can remove tasks from the list.
- **Data Persistence**: Tasks are stored in `localStorage`, ensuring that they remain after the page is refreshed.

## Code Structure

### HTML
- **`<input>` for New Task**: Uses `v-model` to bind the input field to the Vue `newTask` data.
- **`<input>` for Date and Time**: Uses `v-model` to bind the `datetime-local` input to the Vue `taskTime` data.
- **Add Task Button**: Calls the `addTask` method to add a new task to the list.
- **Task List**: Uses `v-for` to render each task from the `tasks` array.

### [Vue.js](https://vuejs.org/)
- **Data**:
  - `newTask`: A string to store the new task's text.
  - `taskTime`: A string to store the new task's date and time.
  - `tasks`: An array to store the list of tasks, initialized from `localStorage` if data is available.
  
- **Methods**:
  - `addTask()`: Adds a new task to the `tasks` array and saves the changes to `localStorage`.
  - `toggleTask(index)`: Toggles the completed status of a selected task.
  - `removeTask(index)`: Removes a task from the `tasks` list.
  - `saveTasks()`: Saves the task list to `localStorage`.
  - `formatDate(dateString)`: Formats a date string into a more readable format.

### [Tailwind CSS](https://tailwindcss.com/)
- **Styling**: Uses Tailwind CSS classes to apply modern, responsive styling to UI elements, such as inputs, buttons, and the task list.

## How to Use
1. **Add a Task**:
   - Enter task text in the "Add a new task" input field.
   - (Optional) Choose a date and time for the task.
   - Click the "Add Task" button or press Enter to add the task to the list.

2. **Mark Task as Complete**:
   - Click the "Complete" button next to a task to mark it as completed. The task text will be crossed out.
   - Click the "Undo" button to revert the task to an incomplete status.

3. **Delete a Task**:
   - Click the "Remove" button next to a task to delete it from the list.

## Data Storage
- **LocalStorage**: The app stores the task list in the browser's `localStorage`. This ensures that task data persists even after the page is refreshed or the browser is closed.

## Requirements
- **[Vue.js](https://vuejs.org/)**: This app uses Vue 3, imported via CDN.
- **[Tailwind CSS](https://tailwindcss.com/)**: Tailwind is used for styling, also imported via CDN,

## Tools
- **[Acode](https://acode.app/)**: This application is made on mobile and uses the code editor acode
- **[Gyazo](https://gyazo.com/)**: I use gyazo to upload images on the application
- **[SvgRepo](https://www.svgrepo.com/)**: I use SvgRepo to search for image or icon assets

## Notes
- Ensure your browser supports `localStorage` and the `datetime-local` input type for the best experience.
- This project uses CDN rather than CLI installation, so it may lack advanced configuration features.
- This project has many flaws, my goal in making this is just for practice and fun
