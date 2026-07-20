# <img src="https://images.mindcloud.co/apps/icons/freedcamp-logo-png-seeklogo-363123_1774023989353.png" alt="Freedcamp logo" width="28" height="28"> Freedcamp: Universal API

Freedcamp project management integration with secured API key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freedcamp/latest
- **Category:** Productivity / Project Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://freedcamp.com
- **Vendor API docs:** https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freedcamp/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new task comment in Freedcamp. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves a list of milestones from Freedcamp. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves unread notifications across projects from Freedcamp. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Freedcamp. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Freedcamp. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Freedcamp. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Freedcamp by task ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Freedcamp. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Freedcamp. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Time Records](actions/list-time-records.md) | GET | Retrieves a list of time records from Freedcamp. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Freedcamp. |

