# <img src="https://images.mindcloud.co/apps/icons/jet-api_1774982910496.png" alt="JetAPI logo" width="28" height="28"> JetAPI: Universal API

Send messages and integrate WhatsApp, Telegram, Facebook, and Instagram

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jetAPI/latest
- **Category:** Communication / Team Messaging
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jetapi.io/
- **Vendor API docs:** https://docs.jetapi.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from JetAPI. |

### Bulk Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Delivery](actions/create-bulk-delivery.md) | POST | Creates a new bulk delivery in JetAPI. |

### Chat Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Update Chat Notes](actions/update-chat-notes.md) | PUT | Updates existing chat notes in JetAPI. |

### Chat Dialog

| Action | Method | Description |
| --- | --- | --- |
| [Open Dialog By Phone](actions/open-dialog-by-phone.md) | GET | Retrieves a chat dialog link from JetAPI by phone. |

### Chat Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Link](actions/create-chat-link.md) | POST | Creates a new chat link in JetAPI. |

### Chatter Session

| Action | Method | Description |
| --- | --- | --- |
| [Delete Chatter Session](actions/delete-chatter-session.md) | DELETE | Deletes chatter sessions from JetAPI. |

### Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Create Delivery](actions/create-delivery.md) | POST | Creates a new message delivery in JetAPI. |
| [Get Delivery Status](actions/get-delivery-status.md) | GET | Retrieves delivery status from JetAPI. |
| [Send File](actions/send-file.md) | POST | Creates a new file delivery in JetAPI. |

### Operator

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Phone Operator](actions/lookup-phone-operator.md) | GET | Finds a phone operator in JetAPI by number. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Developer Chat](actions/delete-developer-chat.md) | DELETE | Deletes developer chats from JetAPI. |
| [Open Developer Chat By Phone](actions/open-developer-chat-by-phone.md) | GET | Retrieves a developer chat link from JetAPI by phone. |

### Utm Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Tags](actions/get-utm-tags.md) | GET | Retrieves UTM tags from JetAPI. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in JetAPI. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from JetAPI. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from JetAPI. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from JetAPI. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in JetAPI. |

