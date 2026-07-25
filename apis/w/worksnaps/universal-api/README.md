# <img src="https://images.mindcloud.co/apps/icons/worksnaps-icon_1776344305513.png" alt="Worksnaps logo" width="28" height="28"> Worksnaps: Universal API

Worksnaps is a time tracking and employee monitoring platform for remote teams. This app wraps the official Worksnaps XML REST API for projects, tasks, time entries, assignments, users, and reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/worksnaps/latest
- **Category:** Productivity / Project Management
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.worksnaps.com
- **Vendor API docs:** https://api.worksnaps.com/api_docs/api_overview.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create a new project](actions/create-a-new-project.md) | POST | Creates a new project in Worksnaps. |
| [Delete a project](actions/delete-a-project.md) | DELETE | Deletes an existing project from Worksnaps. |
| [Get a specific project](actions/get-a-specific-project.md) | GET | Retrieves a specific project from Worksnaps. |
| [Get list of projects](actions/get-projects.md) | GET | Retrieves projects for the current user from Worksnaps. |
| [Update an existing project](actions/update-an-existing-project.md) | PUT | Updates an existing project in Worksnaps. |

### Project Report

| Action | Method | Description |
| --- | --- | --- |
| [Get time entry or time summary report](actions/get-time-entry-or-time-summary-report.md) | GET | Retrieves a project time report from Worksnaps. |

### Summary Report

| Action | Method | Description |
| --- | --- | --- |
| [Get the time report of the projects and users you manage](actions/get-the-time-report-of-the-projects-and-users-you-manage.md) | GET | Retrieves managed project time reports from Worksnaps. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create a Task](actions/create-a-task.md) | POST | Creates a new task in a Worksnaps project. |
| [Deletes a task](actions/deletes-a-task.md) | DELETE | Deletes an existing task from a Worksnaps project. |
| [Get a Task](actions/get-a-task.md) | GET | Retrieves a task from a Worksnaps project. |
| [Get Tasks In a Project](actions/get-tasks-in-a-project.md) | GET | Retrieves tasks in a specific Worksnaps project. |
| [Update a Task](actions/update-a-task.md) | PUT | Updates an existing task in a Worksnaps project. |

### Task Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create a task assignment (i.e., assign a user to a task)](actions/create-a-task-assignment-ie-assign-a-user-to-a-task.md) | POST | Creates a task assignment in a Worksnaps project. |
| [Delete a task assignment](actions/delete-a-task-assignment.md) | DELETE | Deletes an existing task assignment from Worksnaps. |
| [Delete a Task Assignment by ID](actions/delete-a-task-assignment-by-id.md) | DELETE | Deletes an existing task assignment from Worksnaps. |
| [Get a task assignment](actions/get-a-task-assignment.md) | GET | Retrieves a task assignment from a Worksnaps project. |
| [Get tasks assignments](actions/get-tasks-assignments.md) | GET | Retrieves task assignments from a Worksnaps project. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Creating offline time entries for a user](actions/creating-offline-time-entries-for-a-user.md) | POST | Creates offline time entries for a user in Worksnaps. |
| [Delete time entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Worksnaps. |
| [For creating offline time entries for YOURSELF](actions/for-creating-offline-time-entries-for-yourself.md) | POST | Creates offline time entries for yourself in Worksnaps. |
| [Get a time entry](actions/get-a-time-entry.md) | GET | Retrieves a time entry from a Worksnaps project. |
| [Get full resolution screenshot URL](actions/get-full-resolution-screenshot-url.md) | GET | Retrieves a full-resolution screenshot URL from Worksnaps. |
| [Get time entries for a user in a project](actions/get-time-entries-for-a-user-in-a-project.md) | GET | Retrieves a user's time entries from a Worksnaps project. |
| [Get time entries in a project (for one or more users)](actions/get-time-entries-in-a-project-for-one-or-more-users.md) | GET | Retrieves time entries from a Worksnaps project. |
| [Update time entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Worksnaps. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create a new user](actions/create-a-new-user.md) | POST | Creates a new user in Worksnaps. |
| [Get a user](actions/get-a-user.md) | GET | Retrieves a user from Worksnaps. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Worksnaps. |
| [Get list of users](actions/get-list-of-users.md) | GET | Retrieves users from Worksnaps. |
| [Update a user](actions/update-a-user.md) | PUT | Updates an existing user in Worksnaps. |

### User Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Create a user assignment (i.e., assign a user to a project)](actions/create-a-user-assignment-ie-assign-a-user-to-a-project.md) | POST | Creates a user assignment in a Worksnaps project. |
| [Delete a user assignment](actions/delete-a-user-assignment.md) | DELETE | Deletes an existing user assignment from Worksnaps. |
| [Get a user assignment](actions/get-a-user-assignment.md) | GET | Retrieves a user assignment from a Worksnaps project. |
| [Get users (i.e., all user assignments) in a project](actions/get-users-ie-all-user-assignments-in-a-project.md) | GET | Retrieves user assignments from a Worksnaps project. |
| [Update a user assignment](actions/update-a-user-assignment.md) | PUT | Updates an existing user assignment in Worksnaps. |

