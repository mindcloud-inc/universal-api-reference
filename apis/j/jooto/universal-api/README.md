# <img src="https://images.mindcloud.co/apps/icons/unnamed_1775056574544.png" alt="Jooto logo" width="28" height="28"> Jooto: Universal API

Jooto is a project and task management platform for boards, tasks, checklists, comments, notifications, and organization data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jooto/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jooto.com/
- **Vendor API docs:** https://www.jooto.com/api/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jooto/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Board Activities](actions/list-board-activities.md) | GET | Retrieves activity history from a specific Jooto board. |
| [List Public Board Activities](actions/list-public-board-activities.md) | GET | Retrieves activity history from a public Jooto board. |
| [List Task Activities](actions/list-task-activities.md) | GET | Retrieves activity logs for a specific task in Jooto. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [List Public Board Attachments](actions/list-public-board-attachments.md) | GET | Retrieves attachments from a public Jooto project board. |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Board](actions/get-board.md) | GET | Retrieves details for a specific Jooto project board. |
| [Get Public Board](actions/get-public-board.md) | GET | Retrieves details for a public Jooto project board. |
| [List Boards](actions/list-boards.md) | GET | Retrieves a list of project boards from Jooto. |
| [List Favorite Boards](actions/list-favorite-boards.md) | GET | Retrieves favorite project boards from Jooto. |
| [List Public Boards](actions/list-public-boards.md) | GET | Retrieves public project boards from Jooto. |
| [List Public Favorite Boards](actions/list-public-favorite-boards.md) | GET | Retrieves favorite boards from Jooto's public API. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |

### Checklist

| Action | Method | Description |
| --- | --- | --- |
| [List Public Task Checklists](actions/list-public-task-checklists.md) | GET | Retrieves checklists for a public task in Jooto. |
| [List Task Checklists](actions/list-task-checklists.md) | GET | Retrieves checklists for a specific task in Jooto. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Public Task Comments](actions/list-public-task-comments.md) | GET | Retrieves comments for a public task in Jooto. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves comments for a specific task in Jooto. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Board Lists](actions/list-board-lists.md) | GET | Retrieves lists from a specific Jooto project board. |
| [List Public Board Lists](actions/list-public-board-lists.md) | GET | Retrieves lists from a public Jooto project board. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate Limit](actions/get-rate-limit.md) | GET | Retrieves current API rate limit details from Jooto. |
| [Get Unread Notification Count](actions/get-unread-notification-count.md) | GET |  |
| [Get Unread System Notification Count](actions/get-unread-system-notification-count.md) | GET |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification](actions/get-notification.md) | GET |  |
| [List Notification Types](actions/list-notification-types.md) | GET |  |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves a list of notifications from Jooto. |
| [List Public Notifications](actions/list-public-notifications.md) | GET | Retrieves a list of public notifications from Jooto. |
| [List System Notifications](actions/list-system-notifications.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Settings](actions/get-notification-settings.md) | GET |  |
| [Get Public Board Notification Config](actions/get-public-board-notification-config.md) | GET | Retrieves notification settings for a public Jooto board. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Public User Role](actions/get-public-user-role.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET |  |
| [List My Tasks](actions/list-my-tasks.md) | GET |  |
| [List Public Board Tasks](actions/list-public-board-tasks.md) | GET | Retrieves tasks from a public Jooto project board. |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Search Public Board](actions/search-public-board.md) | GET | Finds tasks within a public Jooto project board. |
| [Search Tasks](actions/search-tasks.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Public User](actions/get-public-user.md) | GET | Retrieves details for a public Jooto user. |
| [List Public Board Users](actions/list-public-board-users.md) | GET | Retrieves users from a public Jooto project board. |
| [List Public Users](actions/list-public-users.md) | GET | Retrieves a list of public users from Jooto. |

