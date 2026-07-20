# <img src="https://images.mindcloud.co/apps/icons/askhandle_1775248217358.png" alt="AskHandle logo" width="28" height="28"> AskHandle: Universal API

Manage AskHandle chat rooms, messages, leads, widgets, keyword notifications, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/askhandle/latest
- **Category:** Support / Ticketing
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.askhandle.com/
- **Vendor API docs:** https://dashboard.askhandle.com/api/v1/docs/api_reference.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Rooms](actions/list-rooms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/list-rooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a new room in AskHandle. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves room records from your AskHandle account. |
| [Retrieve Room](actions/retrieve-room.md) | GET | Retrieves one AskHandle room by label. |
| [Update Room](actions/update-room.md) | PUT | Updates an existing AskHandle room by label. |
| [Update Room Field](actions/update-room-field.md) | PUT | Updates one AskHandle room field by label. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves lead records from your AskHandle account. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in an AskHandle room. |
| [List Messages](actions/list-messages.md) | GET | Retrieves message records from your AskHandle account. |
| [Retrieve Message](actions/retrieve-message.md) | GET | Retrieves one AskHandle message by UUID. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Keyword Notifications](actions/list-keyword-notifications.md) | GET | Retrieves keyword notifications from your AskHandle account. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in AskHandle. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing AskHandle webhook by UUID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook records from your AskHandle account. |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET | Retrieves one AskHandle webhook by UUID. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing AskHandle webhook by UUID. |
| [Update Webhook Field](actions/update-webhook-field.md) | PUT | Updates one AskHandle webhook field by UUID. |

