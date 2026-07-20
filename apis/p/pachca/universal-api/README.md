# <img src="https://images.mindcloud.co/apps/icons/favicon-dev-pachca-com-48x48-1_1777386576752.png" alt="Pachca logo" width="28" height="28"> Pachca: Universal API

Pachca is a corporate messenger API for workspace communication, employee management, chats, messages, tasks, bots, webhooks, and security events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pachca/latest
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pachca.com/
- **Vendor API docs:** https://dev.pachca.com/guides/authorization

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get token info](actions/get-token-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachca/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create chat](actions/create-chat.md) | POST |  |
| [Get chat](actions/get-chat.md) | GET |  |
| [List chats](actions/list-chats.md) | GET |  |
| [Search chats](actions/search-chats.md) | GET |  |

### Chat Member

| Action | Method | Description |
| --- | --- | --- |
| [List chat members](actions/list-chat-members.md) | GET |  |

### Custom Property

| Action | Method | Description |
| --- | --- | --- |
| [List custom properties](actions/list-custom-properties.md) | GET |  |

### Group Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get group tag](actions/get-group-tag.md) | GET |  |
| [List group tags](actions/list-group-tags.md) | GET |  |

### Group Tag User

| Action | Method | Description |
| --- | --- | --- |
| [List group tag users](actions/list-group-tag-users.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create message](actions/create-message.md) | POST |  |
| [Delete message](actions/delete-message.md) | DELETE |  |
| [Get message](actions/get-message.md) | GET |  |
| [List messages](actions/list-messages.md) | GET |  |
| [Search messages](actions/search-messages.md) | GET |  |
| [Update message](actions/update-message.md) | PUT |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get profile](actions/get-profile.md) | GET |  |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [List message reactions](actions/list-message-reactions.md) | GET |  |

### Read Member Id

| Action | Method | Description |
| --- | --- | --- |
| [List message read member IDs](actions/list-message-read-member-ids.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get profile status](actions/get-profile-status.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create task](actions/create-task.md) | POST |  |
| [Delete task](actions/delete-task.md) | DELETE |  |
| [Get task](actions/get-task.md) | GET |  |
| [List tasks](actions/list-tasks.md) | GET |  |
| [Update task](actions/update-task.md) | PUT |  |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get thread](actions/get-thread.md) | GET |  |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Get token info](actions/get-token-info.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get user](actions/get-user.md) | GET |  |
| [List users](actions/list-users.md) | GET |  |
| [Search users](actions/search-users.md) | GET |  |

