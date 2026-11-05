# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a REST API with FastAPI to create, read, update, and delete task records. Practice defining request models, using HTTP methods and status codes, and validating API behavior.

## 📝 Tasks

### 🛠️ Create the Task API

#### Description
Create a FastAPI application that stores task records in memory and provides endpoints for listing and creating tasks.

#### Requirements
Completed program should:

- Define a task request model with a required task name and an optional completed flag that defaults to `false`.
- Implement `GET /tasks` to return all tasks and `POST /tasks` to create a task with a unique ID.
- Return HTTP `201 Created` when a task is successfully created.


### 🛠️ Add Endpoints for Individual Tasks

#### Description
Extend the API so clients can retrieve, replace, and delete a task by its ID.

#### Requirements
Completed program should:

- Implement `GET /tasks/{task_id}`, `PUT /tasks/{task_id}`, and `DELETE /tasks/{task_id}`.
- Return HTTP `404 Not Found` when a requested task ID does not exist.
- Return the updated task after a successful `PUT`, and confirm successful deletion with an appropriate response.
- Run the application and verify the endpoints using FastAPI's interactive documentation at `/docs`.
