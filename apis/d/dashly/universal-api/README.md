# <img src="https://images.mindcloud.co/apps/icons/dashly_1774635033262.png" alt="Dashly logo" width="28" height="28"> Dashly: Universal API

Manage live chat, leads, and customer conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dashly/latest
- **Category:** Marketing
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dashly.io/
- **Vendor API docs:** https://developers.dashly.io/webapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Channels](actions/list-channels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/list-channels?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from a Dashly app. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Parts](actions/get-conversation-parts.md) | GET | Retrieves parts from a Dashly conversation. |
| [Reply In Conversation](actions/reply-in-conversation.md) | POST | Creates a reply in a Dashly conversation. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Tag](actions/add-conversation-tag.md) | PUT | Adds a tag to a Dashly conversation. |
| [Assign Conversation](actions/assign-conversation.md) | PUT | Updates a conversation assignment in Dashly. |
| [Close Conversation](actions/close-conversation.md) | PUT | Updates a Dashly conversation to closed status. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a Dashly conversation by ID. |
| [List App Conversations](actions/list-app-conversations.md) | GET | Retrieves conversations from a Dashly app. |
| [List User Conversations](actions/list-user-conversations.md) | GET | Retrieves conversations for a Dashly user. |
| [Remove Conversation Tag](actions/remove-conversation-tag.md) | DELETE | Deletes a tag from a Dashly conversation. |
| [Send Manual Message To User](actions/send-manual-message-to-user.md) | POST | Sends a manual message to a Dashly user. |
| [Set Conversation Typing Indicator](actions/set-conversation-typing-indicator.md) | PUT | Sets the typing indicator in a Dashly conversation. |
| [Start Conversation For User](actions/start-conversation-for-user.md) | POST | Starts a conversation on behalf of a Dashly user. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List User Events](actions/list-user-events.md) | GET | Retrieves events for a Dashly user. |
| [Track User Event](actions/track-user-event.md) | POST | Tracks an event for a Dashly user. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a Dashly user by identifier. |
| [Import User Properties from CSV](actions/import-user-properties-from-csv.md) | POST | Imports user properties into Dashly from CSV. |
| [List Active Users](actions/list-active-users.md) | GET | Retrieves active users from a Dashly app. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Dashly app. |
| [Set User Presence](actions/set-user-presence.md) | PUT | Sends a heartbeat signal for a Dashly user. |
| [Set User Properties](actions/set-user-properties.md) | PUT | Updates properties for a Dashly user. |

