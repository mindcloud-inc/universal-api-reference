# <img src="https://images.mindcloud.co/apps/icons/1a5a0497-c431-45f9-953d-41c3f58215ee_1775152776702.png" alt="Chatwork logo" width="28" height="28"> Chatwork: Universal API

Chat, manage tasks, and share files in Chatwork

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatwork/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://go.chatwork.com/en
- **Vendor API docs:** https://developer.chatwork.com/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Chat](actions/create-group-chat.md) | POST |  |
| [Get Chat](actions/get-chat.md) | GET |  |
| [Leave or Delete Chat](actions/leave-or-delete-chat.md) | DELETE |  |
| [List Chats](actions/list-chats.md) | GET |  |
| [Update Chat](actions/update-chat.md) | PUT |  |

### Chat Member

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Members](actions/list-chat-members.md) | GET |  |
| [Update Chat Members](actions/update-chat-members.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat File](actions/get-chat-file.md) | GET |  |
| [List Chat Files](actions/list-chat-files.md) | GET |  |
| [Upload Chat File](actions/upload-chat-file.md) | POST |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Chat Message](actions/delete-chat-message.md) | DELETE |  |
| [Get Chat Message](actions/get-chat-message.md) | GET |  |
| [List Chat Messages](actions/list-chat-messages.md) | GET |  |
| [Post Chat Message](actions/post-chat-message.md) | POST |  |
| [Update Chat Message](actions/update-chat-message.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Mark Message Unread](actions/mark-message-unread.md) | PUT |  |
| [Mark Messages Read](actions/mark-messages-read.md) | PUT |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get My Status](actions/get-my-status.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Task](actions/create-chat-task.md) | POST |  |
| [Get Chat Task](actions/get-chat-task.md) | GET |  |
| [List Chat Tasks](actions/list-chat-tasks.md) | GET |  |
| [List My Tasks](actions/list-my-tasks.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Update Chat Task Completion Status](actions/update-chat-task-completion-status.md) | PUT |  |

