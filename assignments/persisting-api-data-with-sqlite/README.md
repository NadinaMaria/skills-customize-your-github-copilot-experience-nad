# 📘 Assignment: Persisting API Data with SQLite

## 🎯 Objective

Extend the FastAPI task API to store task records in a SQLite database instead of memory. Practice creating a database table, connecting API endpoints to stored data, and verifying that records survive an application restart.

## 📝 Tasks

### 🛠️ Create the SQLite Database

#### Description
Set up a SQLite database for the task API using Python's built-in `sqlite3` module. Define a table that can store each task's ID, name, and completed status.

#### Requirements
Completed program should:

- Create or open a database file when the application starts or handles a request.
- Create a `tasks` table with an integer primary key, a required task name, and a completed status.
- Store the completed status in SQLite and convert it to a Python boolean when returning task data.


### 🛠️ Connect the API Endpoints to SQLite

#### Description
Replace the in-memory task storage with database queries so the existing task API reads and changes persistent records.

#### Requirements
Completed program should:

- Use the database for `GET /tasks`, `POST /tasks`, `GET /tasks/{task_id}`, `PUT /tasks/{task_id}`, and `DELETE /tasks/{task_id}`.
- Preserve the existing response behavior, including `201 Created` for creation and `404 Not Found` for an unknown task ID.
- Commit database changes after creating, updating, or deleting a task, and return task data in the existing API response format.


### 🛠️ Verify Persistence Across Restarts

#### Description
Run the API, create and update tasks, then restart the application to confirm that the database retains the changes.

#### Requirements
Completed program should:

- Create a task and confirm it appears in `GET /tasks`.
- Stop and restart the API, then confirm the task is still available with its saved values.
- Update and delete a task, then confirm those changes are reflected by subsequent requests.
