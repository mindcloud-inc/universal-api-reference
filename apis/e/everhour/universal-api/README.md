# <img src="https://images.mindcloud.co/apps/icons/download_1774026116869.png" alt="Everhour logo" width="28" height="28"> Everhour: Universal API

Track time, manage projects, budgets, and invoices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/everhour/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://everhour.com
- **Vendor API docs:** https://everhour.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Archive or Unarchive Project](actions/archive-or-unarchive-project.md) | PUT | Archives or unarchives a project in Everhour. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Everhour. |
| [Get Project](actions/get-project.md) | GET | Retrieves a specific project from Everhour. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Everhour. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Everhour. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Everhour. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Everhour. |
| [Get Task](actions/get-task.md) | GET | Retrieves a specific task from Everhour. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves tasks for a project from Everhour. |
| [Search Project Tasks](actions/search-project-tasks.md) | GET | Finds project tasks in Everhour by search query. |
| [Search Tasks](actions/search-tasks.md) | GET | Finds tasks in Everhour by search query. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Everhour. |

### Time Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Time](actions/add-time.md) | POST | Creates a new time record in Everhour. |
| [Delete Time Record](actions/delete-time-record.md) | DELETE | Deletes an existing time record from Everhour. |
| [List Project Time Records](actions/list-project-time-records.md) | GET | Retrieves time records for a project from Everhour. |
| [List Task Time Records](actions/list-task-time-records.md) | GET | Retrieves time records for a task from Everhour. |
| [List Time Records](actions/list-time-records.md) | GET | Retrieves time records from Everhour. |
| [List User Time Records](actions/list-user-time-records.md) | GET | Retrieves time records for a user from Everhour. |
| [Update Time Record](actions/update-time-record.md) | PUT | Updates an existing time record in Everhour. |

### Timer

| Action | Method | Description |
| --- | --- | --- |
| [Get Running Timer](actions/get-running-timer.md) | GET | Retrieves the running timer from Everhour. |
| [Start Timer](actions/start-timer.md) | POST | Starts a timer in Everhour. |
| [Stop Timer](actions/stop-timer.md) | DELETE | Stops the running timer in Everhour. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Everhour. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Everhour. |

