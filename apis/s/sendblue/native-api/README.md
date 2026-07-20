# Sendblue: Native API Reference

A consolidated summary of Sendblue's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.sendblue.com/api/
- **API base URL:** `https://api.sendblue.co`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **API Key ID:** `apiKeyId` · required · Your Sendblue API key ID from the Sendblue dashboard API settings.

Send these headers with each API request:

```http
sb-api-key-id: <apiKeyId>
sb-api-secret-key: <apiKey>
```

[Official authentication documentation](https://docs.sendblue.com/getting-started/credentials/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Webhooks](actions/add-webhooks.md) | `POST /api/account/webhooks` | [docs](https://docs.sendblue.com/api/resources/webhooks/methods/create/) |
| [Create Contact](actions/create-contact.md) | `POST /api/v2/contacts` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/create/) |
| [Create Multiple Contacts](actions/create-multiple-contacts.md) | `POST /api/v2/contacts/bulk` | [docs](https://docs.sendblue.com/api/resources/contacts/subresources/bulk/methods/create/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/v2/contacts/:phone_number` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/delete/) |
| [Delete Message](actions/delete-message.md) | `DELETE /api/message/:message_handle` | [docs](https://docs.sendblue.com/api-v2/messages/) |
| [Delete Multiple Contacts](actions/delete-multiple-contacts.md) | `DELETE /api/v2/contacts` | [docs](https://docs.sendblue.com/api/resources/contacts/subresources/bulk/methods/delete/) |
| [Delete Webhooks](actions/delete-webhooks.md) | `DELETE /api/account/webhooks` | [docs](https://docs.sendblue.com/api/resources/webhooks/methods/delete/) |
| [Direct File Upload](actions/direct-file-upload.md) | `POST /api/upload-file` | [docs](https://docs.sendblue.com/api-v2/media/) |
| [Get Contact](actions/get-contact.md) | `GET /api/v2/contacts/:phone_number` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/retrieve/) |
| [Get Contact Count](actions/get-contact-count.md) | `GET /api/v2/contacts/count` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/count/) |
| [Get Message](actions/get-message.md) | `GET /api/v2/messages/:message_id` | [docs](https://docs.sendblue.com/api/resources/messages/methods/retrieve/) |
| [Get Message Status](actions/get-message-status.md) | `GET /api/status` | [docs](https://docs.sendblue.com/api/resources/messages/methods/get_status/) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v2/contacts` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/list/) |
| [List Messages](actions/list-messages.md) | `GET /api/v2/messages` | [docs](https://docs.sendblue.com/api/resources/messages/methods/list/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/account/webhooks` | [docs](https://docs.sendblue.com/api/resources/webhooks/methods/list/) |
| [Lookup Phone Number](actions/lookup-phone-number.md) | `GET /api/evaluate-service` | [docs](https://docs.sendblue.com/api/resources/lookups/methods/lookup_number/) |
| [Replace Webhooks](actions/replace-webhooks.md) | `PUT /api/account/webhooks` | [docs](https://docs.sendblue.com/api/resources/webhooks/methods/update/) |
| [Send Group Message](actions/send-group-message.md) | `POST /api/send-group-message` | [docs](https://docs.sendblue.com/api/resources/groups/methods/send_message/) |
| [Send Message](actions/send-message.md) | `POST /api/send-message` | [docs](https://docs.sendblue.com/api/resources/messages/methods/send/) |
| [Send Reaction](actions/send-reaction.md) | `POST /api/send-reaction` | [docs](https://docs.sendblue.com/api-v2/reactions/) |
| [Send Read Receipt](actions/send-read-receipt.md) | `POST /api/mark-read` | [docs](https://docs.sendblue.com/api-v2/read-receipts/) |
| [Send Typing Indicator](actions/send-typing-indicator.md) | `POST /api/send-typing-indicator` | [docs](https://docs.sendblue.com/api-v2/typing-indicators/) |
| [Update Contact](actions/update-contact.md) | `PUT /api/v2/contacts/:phone_number` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/update/) |
| [Upload Media Object](actions/upload-media-object.md) | `POST /api/upload-media-object` | [docs](https://docs.sendblue.com/api/resources/media_objects/methods/upload/) |
| [Verify Contact](actions/verify-contact.md) | `POST /api/v2/contacts/verify` | [docs](https://docs.sendblue.com/api/resources/contacts/methods/verify/) |
