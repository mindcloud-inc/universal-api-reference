# <img src="https://images.mindcloud.co/apps/icons/checkvist_1774020617637.png" alt="Checkvist logo" width="28" height="28"> Checkvist: Universal API

Manage checklists, tasks, notes, and due dates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/checkvist/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://checkvist.com
- **Vendor API docs:** https://checkvist.com/auth/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Checklists

| Action | Method | Description |
| --- | --- | --- |
| [Create Checklist](actions/create-checklist.md) | POST | Creates a checklist in Checkvist. |
| [Delete Checklist](actions/delete-checklist.md) | DELETE | Deletes a checklist from Checkvist. |
| [Get Checklist](actions/get-checklist.md) | GET | Retrieves a checklist from Checkvist. |
| [List Checklists](actions/list-checklists.md) | GET | Retrieves checklists from Checkvist. |
| [Update Checklist](actions/update-checklist.md) | PUT | Updates a checklist in Checkvist. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Note](actions/create-task-note.md) | POST | Creates a task note in Checkvist. |
| [Delete Task Note](actions/delete-task-note.md) | DELETE | Deletes a task note from Checkvist. |
| [List Task Notes](actions/list-task-notes.md) | GET | Retrieves task notes from Checkvist. |
| [Update Task Note](actions/update-task-note.md) | PUT | Updates a task note in Checkvist. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Change Task Status](actions/change-task-status.md) | PUT | Updates a task status in Checkvist. |
| [Create Task](actions/create-task.md) | POST | Creates a task in Checkvist. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from Checkvist. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Checkvist. |
| [Import Tasks](actions/import-tasks.md) | POST | Imports tasks into a checklist in Checkvist. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Checkvist. |
| [Set Repeating Task](actions/set-repeating-task.md) | PUT | Sets repeating task details in Checkvist. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Checkvist. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Checkvist. |

