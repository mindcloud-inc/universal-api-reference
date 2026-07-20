# <img src="https://images.mindcloud.co/apps/icons/tick-tick_1772656796149.png" alt="TickTick logo" width="28" height="28"> TickTick: Universal API

Capture tasks, plan schedules, track habits, and manage lists.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tickTick/latest
- **Category:** Support / Ticketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ticktick.com
- **Vendor API docs:** https://developer.ticktick.com/docs/index.html#/openapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List User Projects](actions/list-user-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/list-user-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in TickTick. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from TickTick. |
| [Get Project By ID](actions/get-project-by-id.md) | GET | Retrieves a project from TickTick by ID. |
| [Get Project With Data](actions/get-project-with-data.md) | GET | Retrieves a project with its tasks and columns from TickTick. |
| [List User Projects](actions/list-user-projects.md) | GET | Retrieves the user's projects from TickTick. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in TickTick. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | PUT | Marks a task as complete in TickTick. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in TickTick. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from TickTick. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from TickTick by project and task ID. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in TickTick. |

