# <img src="https://images.mindcloud.co/apps/icons/pachca-admin_1782741577526.png" alt="Pachca (Admin) logo" width="28" height="28"> Pachca (Admin): Universal API

Manage Pachca chats, users, messages, and tasks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pachcaAdmin/latest
- **Category:** Communication / Team Messaging
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pachca.com
- **Vendor API docs:** https://dev.pachca.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Info](actions/get-token-info.md) | GET | Retrieves token information from the Pachca Admin API. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Events](actions/list-audit-events.md) | GET | Retrieves audit events from the Pachca Admin API. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Archive Chat](actions/archive-chat.md) | PUT | Archives a chat in the Pachca Admin API. |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in the Pachca Admin API. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from the Pachca Admin API. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from the Pachca Admin API. |
| [Search Chats](actions/search-chats.md) | GET | Finds chats in the Pachca Admin API by search query. |
| [Unarchive Chat](actions/unarchive-chat.md) | PUT | Unarchives a chat in the Pachca Admin API. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in the Pachca Admin API. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat Export](actions/get-chat-export.md) | GET | Retrieves a chat export from the Pachca Admin API. |
| [Request Chat Export](actions/request-chat-export.md) | POST | Requests a chat export from the Pachca Admin API. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in the Pachca Admin API. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from the Pachca Admin API. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from the Pachca Admin API. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from the Pachca Admin API. |
| [Search Messages](actions/search-messages.md) | GET | Finds messages in the Pachca Admin API by search query. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing message in the Pachca Admin API. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Add Reaction](actions/add-reaction.md) | POST | Creates a new reaction in the Pachca Admin API. |
| [List Reactions](actions/list-reactions.md) | GET | Retrieves reactions from the Pachca Admin API. |
| [Remove Reaction](actions/remove-reaction.md) | DELETE | Deletes a reaction from the Pachca Admin API. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Chat Group Tags](actions/add-chat-group-tags.md) | PUT |  |
| [Create Group Tag](actions/create-group-tag.md) | POST | Creates a new group tag in the Pachca Admin API. |
| [Delete Group Tag](actions/delete-group-tag.md) | DELETE | Deletes a group tag from the Pachca Admin API. |
| [Get Group Tag](actions/get-group-tag.md) | GET | Retrieves a group tag from the Pachca Admin API. |
| [List Group Tags](actions/list-group-tags.md) | GET | Retrieves group tags from the Pachca Admin API. |
| [Remove Chat Group Tag](actions/remove-chat-group-tag.md) | PUT |  |
| [Update Group Tag](actions/update-group-tag.md) | PUT | Updates an existing group tag in the Pachca Admin API. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in the Pachca Admin API. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from the Pachca Admin API. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from the Pachca Admin API. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from the Pachca Admin API. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in the Pachca Admin API. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST | Creates a new thread in the Pachca Admin API. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a thread from the Pachca Admin API. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Chat Members](actions/add-chat-members.md) | POST | Adds chat members in the Pachca Admin API. |
| [Clear Current Status](actions/clear-user-status.md) | DELETE | Deletes your current status from the Pachca Admin API. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your profile from the Pachca Admin API. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from the Pachca Admin API. |
| [Get Current Status](actions/get-user-status.md) | GET | Retrieves your current status from the Pachca Admin API. |
| [List Chat Members](actions/list-chat-members.md) | GET | Retrieves chat members from the Pachca Admin API. |
| [List Group Tag Users](actions/list-group-tag-users.md) | GET |  |
| [List Users](actions/list-users.md) | GET | Retrieves users from the Pachca Admin API. |
| [Remove Chat Member](actions/remove-chat-member.md) | DELETE | Removes a chat member from the Pachca Admin API. |
| [Search Users](actions/search-users.md) | GET | Finds users in the Pachca Admin API by search query. |
| [Set Current Status](actions/set-user-status.md) | PUT | Updates your current status in the Pachca Admin API. |
| [Update Chat Member Role](actions/update-chat-member-role.md) | PUT |  |

