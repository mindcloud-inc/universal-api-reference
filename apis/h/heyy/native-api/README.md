# Heyy: Native API Reference

A consolidated summary of Heyy's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.heyy.io/api-reference/overview
- **API base URL:** `https://api.heyy.io/api/v2.0/`

## Authentication

### Bearer Token

Inject the Heyy API key explicitly as an Authorization bearer header at runtime.

### Credentials

- **API Key:** `apiKey` · optional · Your Heyy API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.heyy.io/api-reference/introduction)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Attribute](actions/add-contact-attribute.md) | `POST /contacts/:contactId/attributes` | [docs](https://docs.heyy.io/api-reference/add-contact-attribute) |
| [Add Recipients To Broadcast](actions/add-recipients-to-broadcast.md) | `POST /[:channelId]/broadcasts/:broadcastId/recipients` | [docs](https://docs.heyy.io/api-reference/add-recipients-to-broadcast) |
| [Create API Webhook](actions/create-api-webhook.md) | `POST /api_webhooks` | [docs](https://docs.heyy.io/api-reference/create-api-webhook) |
| [Create Attribute](actions/create-attribute.md) | `POST /attributes` | [docs](https://docs.heyy.io/api-reference/create-attribute) |
| [Create Broadcast](actions/create-broadcast.md) | `POST /[:channelId]/broadcasts` | [docs](https://docs.heyy.io/api-reference/create-broadcast) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.heyy.io/api-reference/create-contact) |
| [Create Label](actions/create-label.md) | `POST /labels` | [docs](https://docs.heyy.io/api-reference/create-label) |
| [Delete API Webhook](actions/delete-api-webhook.md) | `DELETE /api_webhooks/:webhookId` | [docs](https://docs.heyy.io/api-reference/delete-api-webhook) |
| [Delete Attribute](actions/delete-attribute.md) | `DELETE /attributes/:attributeId` | [docs](https://docs.heyy.io/api-reference/delete-attribute) |
| [Delete Broadcast](actions/delete-broadcast.md) | `DELETE /[:channelId]/broadcasts/:broadcastId` | [docs](https://docs.heyy.io/api-reference/delete-broadcast) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactId` | [docs](https://docs.heyy.io/api-reference/delete-contact) |
| [Delete Label](actions/delete-label.md) | `DELETE /labels/:labelId` | [docs](https://docs.heyy.io/api-reference/delete-label) |
| [Get Broadcast by ID](actions/get-broadcast-by-id.md) | `GET /[:channelId]/broadcasts/:broadcastId` | [docs](https://docs.heyy.io/api-reference/get-broadcast-by-id) |
| [Get Business](actions/get-business.md) | `GET /business` | [docs](https://docs.heyy.io/api-reference/get-business) |
| [Get Channel by ID](actions/get-channel-by-id.md) | `GET /channels/:channelId` | [docs](https://docs.heyy.io/api-reference/get-channel-by-id) |
| [Get Chat by ID](actions/get-chat-by-id.md) | `GET /[:channelId]/chats/:chatId` | [docs](https://docs.heyy.io/api-reference/get-chat-by-id) |
| [Get Contact by ID](actions/get-contact-by-id.md) | `GET /contacts/:contactId` | [docs](https://docs.heyy.io/api-reference/get-contact-by-id) |
| [List API Webhooks](actions/list-api-webhooks.md) | `GET /api_webhooks` | [docs](https://docs.heyy.io/api-reference/get-api-webhooks) |
| [List Attributes](actions/list-attributes.md) | `GET /attributes` | [docs](https://docs.heyy.io/api-reference/get-attributes) |
| [List Automations](actions/list-automations.md) | `GET /[:channelId]/workflows` | [docs](https://docs.heyy.io/api-reference/get-automations) |
| [List Broadcast Recipients](actions/list-broadcast-recipients.md) | `GET /[:channelId]/broadcasts/:broadcastId/recipients` | [docs](https://docs.heyy.io/api-reference/get-broadcast-recipients) |
| [List Broadcasts](actions/list-broadcasts.md) | `GET /[:channelId]/broadcasts` | [docs](https://docs.heyy.io/api-reference/get-broadcasts) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://docs.heyy.io/api-reference/get-channels) |
| [List Chats](actions/list-chats.md) | `GET /[:channelId]/chats` | [docs](https://docs.heyy.io/api-reference/get-chats) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.heyy.io/api-reference/get-contacts) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://docs.heyy.io/api-reference/get-labels) |
| [List Message Templates](actions/list-message-templates.md) | `GET /message_templates` | [docs](https://docs.heyy.io/api-reference/get-message-templates) |
| [Remove Contact Attribute](actions/remove-contact-attribute.md) | `DELETE /contacts/:contactId/attributes` | [docs](https://docs.heyy.io/api-reference/remove-contact-attribute) |
| [Remove Recipients From Broadcast](actions/remove-recipients-from-broadcast.md) | `DELETE /[:channelId]/broadcasts/:broadcastId/recipients` | [docs](https://docs.heyy.io/api-reference/remove-recipients-from-broadcast) |
| [Send WhatsApp Message](actions/send-whats-app-message.md) | `POST /[:channelId]/whatsapp_messages/send` | [docs](https://docs.heyy.io/api-reference/send-whatsapp-message) |
| [Start Broadcast](actions/start-broadcast.md) | `POST /[:channelId]/broadcasts/:broadcastId/start` | [docs](https://docs.heyy.io/api-reference/start-broadcast) |
| [Trigger Automation](actions/trigger-automation.md) | `POST /[:channelId]/workflows/:workflowId` | [docs](https://docs.heyy.io/api-reference/trigger-automation) |
| [Update API Webhook](actions/update-api-webhook.md) | `PUT /api_webhooks/:webhookId` | [docs](https://docs.heyy.io/api-reference/update-api-webhook) |
| [Update Broadcast](actions/update-broadcast.md) | `PUT /[:channelId]/broadcasts/:broadcastId` | [docs](https://docs.heyy.io/api-reference/update-broadcast) |
| [Update Chat](actions/update-chat.md) | `PUT /[:channelId]/chats/:chatId` | [docs](https://docs.heyy.io/api-reference/update-chat) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contactId` | [docs](https://docs.heyy.io/api-reference/update-contact) |
| [Upload File](actions/upload-file.md) | `POST /upload_file` | [docs](https://docs.heyy.io/api-reference/upload-file) |
