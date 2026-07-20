# <img src="https://images.mindcloud.co/apps/icons/google-tasks_1772219460914.png" alt="Google Tasks logo" width="28" height="28"> Google Tasks: Universal API

Capture tasks, organize lists, track deadlines, and manage work anywhere.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleTasks/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developers.google.com/workspace/tasks
- **Vendor API docs:** https://developers.google.com/workspace/tasks/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Task Lists](actions/list-task-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleTasks/latest/actions/list-task-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Google Tasks. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Google Tasks. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Google Tasks. |
| [List Tasks](actions/list-tasks.md) | GET | Finds tasks in a Google Tasks list. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Google Tasks. |

### Task List

| Action | Method | Description |
| --- | --- | --- |
| [List Task Lists](actions/list-task-lists.md) | GET | Finds task lists in Google Tasks. |

