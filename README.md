# Todo-FastAPI
| Endpoint | Method | Description | Body Request | Body Response | Error Response |
| -------- | ------ | ----------- | ------------ | ------------- | ----------- |
| /createTask | POST | Create a Task by both ID and Title. | `{ "id": {id}, "title": "{title}", "completed": false }` | `{ "id": {id}, "title": "{title}", "completed": false }` | `{"error": "Task not found"}` |
| /getTaskByID/{task_id} | GET | Get a task by its ID. | - | `{ "id": {id}, "title": "{title}", "completed": {completed} }` | `{"error": "Task not found"}` |
| /getTaskByTitle/{title} | GET | Get a task by its title. | - | `{ "id": {id}, "title": "{title}", "completed": {completed} }` | `{"error": "No tasks found with title '{title}'"}` |
| /deleteByID/{task_id} | DELETE | Delete a task by its ID. | `{ "id": {id}, "title": "{title}", "completed": false }` | `{"message": "Task deleted successfully"}` | - |
| /deleteByTitle/{title} | DELETE | Delete a task by its Title. | `{ "id": {id}, "title": "{title}", "completed": false }` | `{"message": "All tasks with title '{title}' deleted successfully"}`| - |
| /deleteAll | DELETE | Delete every tasks | `{ "id": {id}, "title": "{title}", "completed": false }` | `{"message": "All tasks deleted successfully"}` | - |
| /getAllTasks | GET | Get every tasks | `{ "id": {id}, "title": "{title}", "completed": false }` | `{ "id": {id}, "title": "{title}", "completed": false }` | - |
| /updateTask/{task_id} | PUT | Update a task by requesting a new data | `{ "id": {id}, "title": "{title}", "completed": {completed} }` | `{"message": "Task updated successfully"}` | `{"error": "Task not found"}`|
