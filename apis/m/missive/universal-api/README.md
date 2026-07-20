# <img src="https://images.mindcloud.co/apps/icons/missive_1773678918738.png" alt="Missive logo" width="28" height="28"> Missive: Universal API

Manage shared inboxes, conversations, and team collaboration

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/missive/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://missiveapp.com
- **Vendor API docs:** https://missiveapp.com/docs/developers/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Conversation](actions/get-conversation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-conversation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Comments](actions/list-conversation-comments.md) | GET | Retrieves comments from a Missive conversation. |

### Contact Book

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Books](actions/list-contact-books.md) | GET | Retrieves contact books from your Missive workspace. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from your Missive workspace. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from your Missive workspace. |
| [Merge Conversations](actions/merge-conversations.md) | PUT | Merges conversations in your Missive workspace. |

### Draft

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft](actions/create-draft.md) | POST | Creates a draft in your Missive workspace. |
| [Delete Draft](actions/delete-draft.md) | DELETE | Deletes a draft from your Missive workspace. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Incoming Message](actions/create-incoming-message.md) | POST | Creates an incoming message in your Missive workspace. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from your Missive workspace. |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves messages from a Missive conversation. |
| [Search Messages by Email Message ID](actions/search-messages-by-email-message-id.md) | GET | Finds Missive messages by email message ID. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your Missive workspace. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a post in your Missive workspace. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes a post from your Missive workspace. |
| [List Conversation Posts](actions/list-conversation-posts.md) | GET | Retrieves posts from a Missive conversation. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a response in your Missive workspace. |
| [Get Response](actions/get-response.md) | GET | Retrieves a response from your Missive workspace. |
| [List Responses](actions/list-responses.md) | GET | Retrieves responses from your Missive workspace. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in your Missive workspace. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from your Missive workspace. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Missive workspace. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in your Missive workspace. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from your Missive workspace. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Missive workspace. |

