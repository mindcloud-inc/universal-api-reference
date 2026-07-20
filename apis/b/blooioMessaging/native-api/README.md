# Blooio Messaging: Native API Reference

A consolidated summary of Blooio Messaging's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.blooio.com/
- **API base URL:** `https://backend.blooio.com/v2/api`

## Authentication

### API Key

Use a Blooio API key with Bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.blooio.com/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Tags](actions/add-contact-tags.md) | `POST /contacts/{identifier}/tags` | [docs](https://docs.blooio.com/contacts/addContactTags) |
| [Check Contact Capabilities](actions/check-contact-capabilities.md) | `GET /contacts/{identifier}/capabilities` | [docs](https://docs.blooio.com/contacts/getContactCapabilities) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.blooio.com/contacts/createContact) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://docs.blooio.com/groups/createGroup) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.blooio.com/webhooks/createWebhook) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{identifier}` | [docs](https://docs.blooio.com/contacts/deleteContact) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/{groupId}` | [docs](https://docs.blooio.com/groups/deleteGroup) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{identifier}` | [docs](https://docs.blooio.com/contacts/getContact) |
| [Get Current Authentication Context](actions/get-current-authentication-context.md) | `GET /me` | [docs](https://docs.blooio.com/account/getMe) |
| [Get Group](actions/get-group.md) | `GET /groups/{groupId}` | [docs](https://docs.blooio.com/groups/getGroup) |
| [Get Message](actions/get-message.md) | `GET /chats/{chatId}/messages/{messageId}` | [docs](https://docs.blooio.com/messages/getMessage) |
| [Get Message Status](actions/get-message-status.md) | `GET /chats/{chatId}/messages/{messageId}/status` | [docs](https://docs.blooio.com/messages/getMessageStatus) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhookId}` | [docs](https://docs.blooio.com/webhooks/getWebhook) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /chats/{chatId}/messages` | [docs](https://docs.blooio.com/messages/listChatMessages) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /contacts/{identifier}/tags` | [docs](https://docs.blooio.com/contacts/listContactTags) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.blooio.com/contacts/listContacts) |
| [List Group Members](actions/list-group-members.md) | `GET /groups/{groupId}/members` | [docs](https://docs.blooio.com/group-members/listGroupMembers) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.blooio.com/groups/listGroups) |
| [List Numbers](actions/list-numbers.md) | `GET /me/numbers` | [docs](https://docs.blooio.com/numbers/listNumbers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.blooio.com/webhooks/listWebhooks) |
| [Remove Contact Tag](actions/remove-contact-tag.md) | `DELETE /contacts/{identifier}/tags/{tag}` | [docs](https://docs.blooio.com/contacts/removeContactTag) |
| [Send Message](actions/send-message.md) | `POST /chats/{chatId}/messages` | [docs](https://docs.blooio.com/messages/sendMessage) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{identifier}` | [docs](https://docs.blooio.com/contacts/updateContact) |
| [Update Group](actions/update-group.md) | `PATCH /groups/{groupId}` | [docs](https://docs.blooio.com/groups/updateGroup) |
