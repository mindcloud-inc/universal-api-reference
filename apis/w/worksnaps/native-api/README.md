# Worksnaps: Native API Reference

A consolidated summary of Worksnaps's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://api.worksnaps.com/api_docs/api_overview.html
- **OpenAPI specification:** https://api.worksnaps.com/api_docs/worksnaps.json
- **API base URL:** `https://api.worksnaps.com/api`

## Authentication

### Basic Auth

Use your Worksnaps API token as the username. The password value is required by HTTP Basic auth but is ignored by Worksnaps.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.worksnaps.com/api_docs/api_overview.html)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml` |
| `Content-Type` | `application/xml` |

Responses from this API use XML.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create a new project](actions/create-a-new-project.md) | `POST /projects.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Create a new user](actions/create-a-new-user.md) | `POST /users.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Create a Task](actions/create-a-task.md) | `POST /projects/{project_id}/tasks.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Create a task assignment (i.e., assign a user to a task)](actions/create-a-task-assignment-ie-assign-a-user-to-a-task.md) | `POST /projects/{project_id}/task_assignments.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Create a user assignment (i.e., assign a user to a project)](actions/create-a-user-assignment-ie-assign-a-user-to-a-project.md) | `POST /projects/{project_id}/user_assignments.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Creating offline time entries for a user](actions/creating-offline-time-entries-for-a-user.md) | `POST /projects/{project_id}/users/{user_id}/time_entries.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Delete a project](actions/delete-a-project.md) | `DELETE /projects/{project_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Delete a task assignment](actions/delete-a-task-assignment.md) | `DELETE /projects/{project_id}/task_assignments.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Delete a Task Assignment by ID](actions/delete-a-task-assignment-by-id.md) | `DELETE /projects/{project_id}/task_assignments/{task_assignment_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Delete a user assignment](actions/delete-a-user-assignment.md) | `DELETE /projects/{project_id}/user_assignments/{user_assignment_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Delete time entry](actions/delete-time-entry.md) | `DELETE /projects/{project_id}/time_entries/{time_entry_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Deletes a task](actions/deletes-a-task.md) | `DELETE /projects/{project_id}/tasks/{task_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [For creating offline time entries for YOURSELF](actions/for-creating-offline-time-entries-for-yourself.md) | `POST /projects/{project_id}/time_entries.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get a specific project](actions/get-a-specific-project.md) | `GET /projects/{project_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get a Task](actions/get-a-task.md) | `GET /projects/{project_id}/tasks/{task_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get a task assignment](actions/get-a-task-assignment.md) | `GET /projects/{project_id}/task_assignments/{task_assignment_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get a time entry](actions/get-a-time-entry.md) | `GET /projects/{project_id}/time_entries/{time_entry_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get a user](actions/get-a-user.md) | `GET /users/{user_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get a user assignment](actions/get-a-user-assignment.md) | `GET /projects/{project_id}/user_assignments/{user_assignment_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get Current User](actions/get-current-user.md) | `GET /me.xml` | [docs](https://api.worksnaps.com/api_docs/dist/index.html#!/User_Account_API/get_me_xml) |
| [Get full resolution screenshot URL](actions/get-full-resolution-screenshot-url.md) | `GET /projects/{project_id}/time_entries/{time_entry_id}.xml?full_resolution_url=1` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get list of users](actions/get-list-of-users.md) | `GET /users.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get list of projects](actions/get-projects.md) | `GET /projects.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get tasks assignments](actions/get-tasks-assignments.md) | `GET /projects/{project_id}/task_assignments.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get Tasks In a Project](actions/get-tasks-in-a-project.md) | `GET /projects/{project_id}/tasks.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get the time report of the projects and users you manage](actions/get-the-time-report-of-the-projects-and-users-you-manage.md) | `GET /summary_reports` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get time entries for a user in a project](actions/get-time-entries-for-a-user-in-a-project.md) | `GET /projects/{project_id}/users/{user_id}/time_entries.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get time entries in a project (for one or more users)](actions/get-time-entries-in-a-project-for-one-or-more-users.md) | `GET /projects/{project_id}/time_entries.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get time entry or time summary report](actions/get-time-entry-or-time-summary-report.md) | `GET /projects/{project_id}/reports` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Get users (i.e., all user assignments) in a project](actions/get-users-ie-all-user-assignments-in-a-project.md) | `GET /projects/{project_id}/user_assignments.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Update a Task](actions/update-a-task.md) | `PUT /projects/{project_id}/tasks/{task_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Update a user](actions/update-a-user.md) | `PUT /users/{user_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Update a user assignment](actions/update-a-user-assignment.md) | `PUT /projects/{project_id}/user_assignments/{user_assignment_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Update an existing project](actions/update-an-existing-project.md) | `PUT /projects/{project_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
| [Update time entry](actions/update-time-entry.md) | `PUT /projects/{project_id}/time_entries/{time_entry_id}.xml` | [docs](https://api.worksnaps.com/api_docs/worksnaps.json) |
