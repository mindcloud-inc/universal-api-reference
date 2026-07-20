# <img src="https://images.mindcloud.co/apps/icons/yanado_1774977720990.png" alt="Yanado logo" width="28" height="28"> Yanado: Universal API

Yanado helps teams manage tasks, email workflows, statuses, users, comments, and notifications directly from Gmail. This MindCloud wrapper covers Yanado's documented public API with API-key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yanado/latest
- **Category:** Productivity / Project Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yanado.com
- **Vendor API docs:** https://api.yanado.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users From Team](actions/list-users-from-team.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yanado/latest/actions/list-users-from-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Yanado. |

### Email Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks With Emails Attached](actions/list-tasks-with-emails-attached.md) | GET | Retrieves tasks with attached emails from Yanado. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Yanado. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Yanado by type. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses From List](actions/list-statuses-from-list.md) | GET | Retrieves statuses from a Yanado list. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Yanado. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Yanado. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Yanado. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Yanado. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users From List](actions/list-users-from-list.md) | GET | Retrieves users from a Yanado list. |
| [List Users From Team](actions/list-users-from-team.md) | GET | Retrieves users from a Yanado team. |

