# <img src="https://images.mindcloud.co/apps/icons/twist_1773852264951.png" alt="Twist logo" width="28" height="28"> Twist: Universal API

Manage Twist workspaces, channels, threads, and async messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/twist/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://twist.com/
- **Vendor API docs:** https://developer.twist.com/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads a new attachment to Twist. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Archive Channel](actions/archive-channel.md) | PUT | Archives an existing channel in Twist. |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Twist. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Twist by ID. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from a Twist workspace. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Twist. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in a Twist thread. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from a Twist thread. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get or Create Conversation](actions/get-or-create-conversation.md) | POST | Finds a Twist conversation, or creates one if needed. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from a Twist workspace. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in a Twist conversation. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from a Twist conversation. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Content](actions/search-content.md) | GET | Finds threads and messages in Twist by query. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST | Creates a new thread in a Twist channel. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a thread from Twist by ID. |
| [List Threads](actions/list-threads.md) | GET | Retrieves threads from a Twist channel or workspace. |
| [List Unread Threads](actions/list-unread-threads.md) | GET | Retrieves unread threads from a Twist workspace. |
| [Mark Thread as Read](actions/mark-thread-as-read.md) | PUT | Marks a Twist thread as read. |
| [Move Thread to Channel](actions/move-thread-to-channel.md) | PUT | Moves a thread to another Twist channel. |
| [Update Thread](actions/update-thread.md) | PUT | Updates an existing thread in Twist. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current authenticated user from Twist. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Workspace](actions/get-default-workspace.md) | GET | Retrieves the default workspace from Twist. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Twist by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves all accessible workspaces from Twist. |

