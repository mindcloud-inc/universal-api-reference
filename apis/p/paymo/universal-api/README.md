# <img src="https://images.mindcloud.co/apps/icons/paymo-icon_1752688818818.png" alt="Paymo logo" width="28" height="28"> Paymo: Universal API

Paymo is an online work and project management platform for managing tasks, team schedules, time tracking, and client billing from one place.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paymo/latest
- **Category:** Productivity / Project Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paymoapp.com/
- **Vendor API docs:** https://github.com/paymo-org/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Paymo. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Paymo. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Paymo. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Paymo. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Paymo. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Paymo. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Paymo. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Paymo. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Paymo. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Paymo. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Paymo. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Paymo. |

### Task List

| Action | Method | Description |
| --- | --- | --- |
| [Create Task List](actions/create-task-list.md) | POST | Creates a task list in Paymo. |
| [Get Task List](actions/get-task-list.md) | GET | Retrieves a task list from Paymo. |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists from Paymo. |
| [Update Task List](actions/update-task-list.md) | PUT | Updates an existing task list in Paymo. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a time entry in Paymo. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Paymo. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Paymo. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Paymo. |

