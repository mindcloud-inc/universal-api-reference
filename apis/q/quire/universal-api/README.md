# <img src="https://images.mindcloud.co/apps/icons/quire_1774303458650.png" alt="Quire logo" width="28" height="28"> Quire: Universal API

Manage projects, tasks, comments, statuses, and tags in Quire

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quire/latest
- **Category:** Productivity / Project Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quire.io/
- **Vendor API docs:** https://quire.io/dev/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Quire. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Quire. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Create Status](actions/create-status.md) | POST | Creates a new status in Quire. |
| [Delete Status](actions/delete-status.md) | DELETE | Deletes an existing status from Quire. |
| [Get Status](actions/get-status.md) | GET | Retrieves a status from a Quire project. |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from a Quire project. |
| [Update Status](actions/update-status.md) | PUT | Updates an existing status in Quire. |

### Subtasks

| Action | Method | Description |
| --- | --- | --- |
| [List Subtasks](actions/list-subtasks.md) | GET | Retrieves subtasks from a Quire task. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Quire. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Quire. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Quire. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from a Quire project. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Quire. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Quire. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Quire. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Quire. |
| [List Root Tasks](actions/list-root-tasks.md) | GET | Retrieves root tasks from a Quire project. |
| [Search Tasks](actions/search-tasks.md) | GET | Finds tasks in a Quire project by search text. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Quire. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Quire. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Quire. |

