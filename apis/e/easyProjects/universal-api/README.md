# <img src="https://images.mindcloud.co/apps/icons/easy-projects_1776198690332.png" alt="Easy Projects logo" width="28" height="28"> Easy Projects: Universal API

Birdview PSA / Easy Projects API wrapper

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyProjects/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://birdviewpsa.com/
- **Vendor API docs:** https://help.birdviewpsa.com/hc/en-us/articles/115001797351-Birdview-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current Easy Projects account details. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customers](actions/get-customers.md) | GET | Retrieves customers visible to the current Easy Projects user. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Priorities](actions/get-priorities.md) | GET | Retrieves task priorities from Easy Projects. |
| [Get Task Types](actions/get-task-types.md) | GET | Retrieves task types from Easy Projects. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get All Projects](actions/get-all-projects.md) | GET | Retrieves projects visible to the current Easy Projects user. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Easy Projects by ID. |
| [Get Project Attachments](actions/get-project-attachments.md) | GET | Retrieves attachments from a specific Easy Projects project. |
| [Get Project Kanban](actions/get-project-kanban.md) | GET | Retrieves the kanban board for an Easy Projects project. |
| [Get Project Members](actions/get-project-members.md) | GET | Retrieves members of a specific Easy Projects project. |
| [Get Project Messages](actions/get-project-messages.md) | GET | Retrieves messages from a specific Easy Projects project. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Statuses](actions/get-project-statuses.md) | GET | Retrieves project statuses from Easy Projects. |
| [Get Task Statuses](actions/get-task-statuses.md) | GET | Retrieves task statuses from Easy Projects. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Message](actions/add-task-message.md) | POST | Creates a new message on an Easy Projects task. |
| [Add Time Entry](actions/add-time-entry.md) | POST | Creates a new time entry for an Easy Projects task. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Easy Projects. |
| [Get All Tasks](actions/get-all-tasks.md) | GET | Retrieves tasks visible to the current Easy Projects user. |
| [Get My Active Tasks](actions/get-my-active-tasks.md) | GET | Retrieves the current user's active Easy Projects tasks. |
| [Get My In Progress Tasks](actions/get-my-in-progress-tasks.md) | GET | Retrieves the current user's in-progress Easy Projects tasks. |
| [Get My Tasks](actions/get-my-tasks.md) | GET | Retrieves the current user's Easy Projects tasks. |
| [Get Project Tasks](actions/get-project-tasks.md) | GET | Retrieves tasks from a specific Easy Projects project. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Easy Projects by ID. |
| [Get Task Attachments](actions/get-task-attachments.md) | GET | Retrieves attachments from an Easy Projects task. |
| [Get Task Messages](actions/get-task-messages.md) | GET | Retrieves messages from an Easy Projects task. |
| [Get Tasks By Projects](actions/get-tasks-by-projects.md) | GET | Retrieves tasks grouped by project in Easy Projects. |
| [Set Task Assignees](actions/set-task-assignees.md) | PUT | Updates assignees for an Easy Projects task. |
| [Set Task Done](actions/set-task-done.md) | PUT | Marks an Easy Projects task as done. |
| [Set Task Status](actions/set-task-status.md) | PUT | Updates the status of an Easy Projects task. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get All Teams](actions/get-all-teams.md) | GET | Retrieves teams visible to the current Easy Projects user. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get All Users](actions/get-all-users.md) | GET | Retrieves users visible to the current Easy Projects user. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the currently signed-in Easy Projects user. |

