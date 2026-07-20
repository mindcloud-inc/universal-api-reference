# <img src="https://images.mindcloud.co/apps/icons/todoist_1772453494370.png" alt="Todoist logo" width="28" height="28"> Todoist: Universal API

Create tasks, organize projects, and track work

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/todoist/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://todoist.com
- **Vendor API docs:** https://developer.todoist.com/api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Todoist. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Todoist. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Todoist. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Todoist. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Todoist. |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from Todoist. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Todoist. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Todoist. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Create Section](actions/create-section.md) | POST | Creates a new section in Todoist. |
| [List Sections](actions/list-sections.md) | GET | Retrieves sections from Todoist. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Todoist. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Close Task](actions/close-task.md) | PUT | Closes an existing task in Todoist. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Todoist. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Todoist. |
| [Get Task](actions/get-task.md) | GET | Retrieves task details from Todoist. |
| [Move Task](actions/move-task.md) | PUT | Moves an existing task in Todoist. |
| [Quick Add](actions/quick-add.md) | POST | Creates a task in Todoist from quick-add text. |
| [Reopen Task](actions/reopen-task.md) | PUT | Reopens an existing task in Todoist. |
| [Search Tasks By Filter](actions/search-tasks-by-filter.md) | GET | Finds tasks in Todoist by filter query. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Todoist. |

