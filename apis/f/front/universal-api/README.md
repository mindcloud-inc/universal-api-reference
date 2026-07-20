# <img src="https://images.mindcloud.co/apps/icons/font-original_1772833275283.png" alt="Front logo" width="28" height="28"> Front: Universal API

Manage shared inbox conversations, contacts, drafts, tags, and comments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/front/latest
- **Category:** Support / Ticketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://front.com
- **Vendor API docs:** https://dev.frontapp.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Token Details](actions/get-api-token-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/get-api-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Assigned Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Assigned Conversations](actions/list-assigned-conversations.md) | GET | Retrieves conversations assigned to a teammate in Front. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves a list of channels from Front. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a conversation comment in Front. |
| [List Conversation Comments](actions/list-conversation-comments.md) | GET | Retrieves a list of conversation comments from Front. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get API Token Details](actions/get-api-token-details.md) | GET | Retrieves API token details from Front. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Front. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Front. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Front. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Conversations](actions/list-contact-conversations.md) | GET | Retrieves a list of contact conversations from Front. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Followers](actions/add-conversation-followers.md) | POST | Adds followers to a conversation in Front. |
| [Add Conversation Tag](actions/add-conversation-tag.md) | POST | Adds a tag to a conversation in Front. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves detailed conversation information from Front. |
| [List Conversation Followers](actions/list-conversation-followers.md) | GET | Retrieves a list of conversation followers from Front. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves a list of conversations from Front. |
| [Remove Conversation Tag](actions/remove-conversation-tag.md) | DELETE | Removes a tag from a conversation in Front. |
| [Search Conversations](actions/search-conversations.md) | GET | Finds conversations in Front by query. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Front. |
| [Update Conversation Assignee](actions/update-conversation-assignee.md) | PUT | Updates a conversation assignee in Front. |

### Drafts

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Reply](actions/create-draft-reply.md) | POST | Creates a draft reply in Front. |
| [Delete Message Draft](actions/delete-message-draft.md) | DELETE | Deletes an existing message draft from Front. |
| [Edit Message Draft](actions/edit-message-draft.md) | PUT | Updates an existing message draft in Front. |
| [List Conversation Drafts](actions/list-conversation-drafts.md) | GET | Retrieves a list of conversation drafts from Front. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET | Retrieves detailed message information from Front. |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves a list of conversation messages from Front. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Notes](actions/list-contact-notes.md) | GET | Retrieves a list of contact notes from Front. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from Front. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves a list of teams from Front. |

### Teammate

| Action | Method | Description |
| --- | --- | --- |
| [Get Teammate](actions/get-teammate.md) | GET | Retrieves detailed teammate information from Front. |
| [List Teammates](actions/list-teammates.md) | GET | Retrieves a list of teammates from Front. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Retrieves a list of views from Front. |

