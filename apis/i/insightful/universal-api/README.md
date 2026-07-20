# <img src="https://images.mindcloud.co/apps/icons/insightful-icon-filled-256_1776796919580.png" alt="Insightful logo" width="28" height="28"> Insightful: Universal API

Insightful is a workforce intelligence and productivity platform for managing employees, teams, projects, tasks, time limits, and operational analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/insightful/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.insightful.io/
- **Vendor API docs:** https://developers.insightful.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Deactivate Employee](actions/deactivate-employee.md) | DELETE | Deactivates an employee in your Insightful account. |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from your Insightful account. |
| [Invite Employee](actions/invite-employee.md) | POST | Invites a new employee to your Insightful account. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from your Insightful account. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in your Insightful account. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from your Insightful account. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your Insightful account. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Insightful account. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in your Insightful account. |

### Shared Setting

| Action | Method | Description |
| --- | --- | --- |
| [Create Shared Setting](actions/create-shared-setting.md) | POST | Creates a new shared setting in Insightful. |
| [Get Shared Setting](actions/get-shared-setting.md) | GET | Retrieves a shared setting from your Insightful account. |
| [List Shared Settings](actions/list-shared-settings.md) | GET | Retrieves shared settings from your Insightful account. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in your Insightful account. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from your Insightful account. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from your Insightful account. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Insightful account. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in your Insightful account. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in your Insightful account. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes a team from your Insightful account. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from your Insightful account. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from your Insightful account. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in your Insightful account. |

### Time Limit

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Limit](actions/create-time-limit.md) | POST | Creates a new time limit in Insightful. |
| [List Time Limits](actions/list-time-limits.md) | GET | Finds time limits in Insightful by project or employee. |

