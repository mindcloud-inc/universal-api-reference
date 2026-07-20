# <img src="https://images.mindcloud.co/apps/icons/favicon-developer-zendesk-com-48x48_1777046701048.png" alt="Sunshine Conversations logo" width="28" height="28"> Sunshine Conversations: Universal API

Sunshine Conversations is Zendesk's messaging platform API for managing conversations, users, integrations, messages, switchboards, webhooks, and related messaging resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sunshineConversations/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zendesk.com/service/messaging/
- **Vendor API docs:** https://developer.zendesk.com/documentation/conversations/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Integrations](actions/list-integrations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-integrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Post Activity](actions/post-activity.md) | POST | Posts conversation activity events to Sunshine Conversations. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get App Key](actions/get-app-key.md) | GET | Retrieves an app API key from Sunshine Conversations. |
| [List App Keys](actions/list-app-keys.md) | GET | Retrieves app API keys from Sunshine Conversations. |
| [List Integration Keys](actions/list-integration-keys.md) | GET | Retrieves integration API keys from Sunshine Conversations. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves app details from Sunshine Conversations. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Sunshine Conversations. |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes a conversation, its messages, and attachments from Sunshine Conversations. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Sunshine Conversations. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves app conversations from Sunshine Conversations. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Sunshine Conversations. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves a user's devices from Sunshine Conversations. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Sunshine Conversations. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves configured integrations from Sunshine Conversations. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from a Sunshine Conversations conversation. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from a Sunshine Conversations conversation. |
| [Post Message](actions/post-message.md) | POST | Creates a new message in a Sunshine Conversations conversation. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves a user's clients from Sunshine Conversations. |
| [List Switchboards](actions/list-switchboards.md) | GET | Retrieves app switchboards from Sunshine Conversations. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Sunshine Conversations. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user, clients, and conversation history from Sunshine Conversations. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Sunshine Conversations. |
| [List Participants](actions/list-participants.md) | GET | Retrieves conversation participants from Sunshine Conversations. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Sunshine Conversations. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves integration webhooks from Sunshine Conversations. |

