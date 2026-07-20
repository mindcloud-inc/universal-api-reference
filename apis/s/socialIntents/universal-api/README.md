# <img src="https://images.mindcloud.co/apps/icons/id-qyac-qwjd-1774549966162_1774549971134.jpeg" alt="Social Intents logo" width="28" height="28"> Social Intents: Universal API

Manage live chat widgets, conversations, offline messages, and leads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/socialIntents/latest
- **Category:** Support / Contact Center
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.socialintents.com
- **Vendor API docs:** https://www.socialintents.com/docs/integrations/rest-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Widgets](actions/list-widgets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Ping API](actions/ping-api.md) | GET | Retrieves API status from Social Intents. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat By ID](actions/get-chat-by-id.md) | GET | Retrieves a chat from Social Intents by ID. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from Social Intents. |
| [List Chats By Date Range](actions/list-chats-by-date-range.md) | GET | Retrieves chats from Social Intents using a date range. |
| [List Chats By Email](actions/list-chats-by-email.md) | GET | Retrieves chats from Social Intents by visitor email. |
| [List Chats By Timezone](actions/list-chats-by-timezone.md) | GET | Retrieves chats from Social Intents by timezone. |
| [List Chats By Visitor](actions/list-chats-by-visitor.md) | GET | Retrieves chats from Social Intents by visitor ID. |
| [List Chats By Widget](actions/list-chats-by-widget.md) | GET | Retrieves chats from Social Intents by widget ID. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts By Date Range](actions/list-contacts-by-date-range.md) | GET | Retrieves contacts from Social Intents using a date range. |
| [List Contacts By Timezone](actions/list-contacts-by-timezone.md) | GET | Retrieves contacts from Social Intents by timezone. |
| [List Contacts By Widget](actions/list-contacts-by-widget.md) | GET | Retrieves contacts from Social Intents by widget ID. |
| [List Contacts / Leads](actions/list-contacts-leads.md) | GET | Retrieves contacts and leads from Social Intents. |

### Missed Chat

| Action | Method | Description |
| --- | --- | --- |
| [List Missed Chats](actions/list-missed-chats.md) | GET | Retrieves missed chats from Social Intents. |
| [List Missed Chats By Date Range](actions/list-missed-chats-by-date-range.md) | GET | Retrieves missed chats from Social Intents using a date range. |
| [List Missed Chats By Email](actions/list-missed-chats-by-email.md) | GET | Retrieves missed chats from Social Intents by visitor email. |
| [List Missed Chats By Timezone](actions/list-missed-chats-by-timezone.md) | GET | Retrieves missed chats from Social Intents by timezone. |
| [List Missed Chats By Visitor](actions/list-missed-chats-by-visitor.md) | GET | Retrieves missed chats from Social Intents by visitor ID. |
| [List Missed Chats By Widget](actions/list-missed-chats-by-widget.md) | GET | Retrieves missed chats from Social Intents by widget ID. |

### Offline Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Offline Message By ID](actions/get-offline-message-by-id.md) | GET | Retrieves an offline message from Social Intents by ID. |
| [List Offline Messages](actions/list-offline-messages.md) | GET | Retrieves offline messages from Social Intents. |
| [List Offline Messages By Date Range](actions/list-offline-messages-by-date-range.md) | GET | Retrieves offline messages from Social Intents using a date range. |
| [List Offline Messages By Email](actions/list-offline-messages-by-email.md) | GET | Retrieves offline messages from Social Intents by visitor email. |
| [List Offline Messages By Timezone](actions/list-offline-messages-by-timezone.md) | GET | Retrieves offline messages from Social Intents by timezone. |
| [List Offline Messages By Visitor](actions/list-offline-messages-by-visitor.md) | GET | Retrieves offline messages from Social Intents by visitor ID. |
| [List Offline Messages By Widget](actions/list-offline-messages-by-widget.md) | GET | Retrieves offline messages from Social Intents by widget ID. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completed Webhook](actions/create-chat-completed-webhook.md) | POST | Creates a chat completed webhook in Social Intents. |
| [Create Lead Captured Webhook](actions/create-lead-captured-webhook.md) | POST | Creates a lead captured webhook in Social Intents. |
| [Create Offline Message Webhook](actions/create-offline-message-webhook.md) | POST | Creates an offline message webhook in Social Intents. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Social Intents. |
| [Delete Widget Webhook](actions/delete-widget-webhook.md) | DELETE | Deletes a widget webhook from Social Intents. |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves widgets from Social Intents. |

