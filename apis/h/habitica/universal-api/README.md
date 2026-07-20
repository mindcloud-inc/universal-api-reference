# <img src="https://images.mindcloud.co/apps/icons/habitica_1775489466258.png" alt="Habitica logo" width="28" height="28"> Habitica: Universal API

Habitica API integration for tasks, tags, user profile, and related productivity workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/habitica/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://habitica.com
- **Vendor API docs:** https://habitica.com/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Read Notifications](actions/read-notifications.md) | PUT | Marks notifications as read in Habitica. |

### Checklist Item

| Action | Method | Description |
| --- | --- | --- |
| [Add Checklist Item](actions/add-checklist-item.md) | POST | Adds a checklist item to a Habitica task. |
| [Remove Checklist Item](actions/remove-checklist-item.md) | DELETE | Deletes a checklist item from Habitica. |
| [Score Checklist Item](actions/score-checklist-item.md) | PUT | Scores a checklist item in Habitica. |
| [Update Checklist Item](actions/update-checklist-item.md) | PUT | Updates a checklist item in Habitica. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Inbox Messages](actions/list-inbox-messages.md) | GET | Retrieves inbox messages from Habitica. |
| [Send Private Message](actions/send-private-message.md) | POST | Sends a private message to a Habitica member. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Buy List](actions/get-inventory-buy-list.md) | GET | Retrieves items available for purchase in Habitica. |
| [List In-App Rewards](actions/list-in-app-rewards.md) | GET | Retrieves in-app rewards from Habitica. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET | Retrieves Habitica API status information. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Habitica. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Habitica. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Habitica. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Habitica. |
| [Reorder Tags](actions/reorder-tags.md) | PUT | Reorders tags in Habitica. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Habitica. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag To Task](actions/add-tag-to-task.md) | PUT | Adds a tag to a Habitica task. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Habitica. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Habitica. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Habitica. |
| [List User Tasks](actions/list-user-tasks.md) | GET | Retrieves the current user's tasks from Habitica. |
| [Remove Tag From Task](actions/remove-tag-from-task.md) | PUT | Removes a tag from a Habitica task. |
| [Score Task](actions/score-task.md) | PUT | Scores a task in Habitica. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Habitica. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current user from Habitica. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Anonymized User Data](actions/get-anonymized-user-data.md) | GET | Retrieves anonymized user data from Habitica. |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from Habitica. |
| [Get Member Achievements](actions/get-member-achievements.md) | GET | Retrieves a member's achievements from Habitica. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Habitica. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Habitica. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Habitica. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Habitica. |

