# 2Chat: Native API Reference

A consolidated summary of 2Chat's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.2chat.co/docs/category/api
- **API base URL:** `https://api.p.2chat.io/open`

## Authentication

### API Key

Authenticate 2Chat API requests with your X-User-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-User-API-Key: <apiKey>
```

[Official authentication documentation](https://developers.2chat.co/docs/API/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `results_per_page` in the query string to set the page size (default 50). Use `page_number` in the query string to choose the page; numbering starts at 0.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Participant](actions/add-participant.md) | `POST /whatsapp/group/:group_uuid/add-participant` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/add-participant) |
| [Check If Number Is On WhatsApp](actions/check-if-number-is-on-whats-app.md) | `GET /whatsapp/check-number/:from_number/:number_to_check` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/check-number) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.2chat.co/docs/API/Contacts/create-contact) |
| [Create Group](actions/create-group.md) | `POST /whatsapp/group/create` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/create-group) |
| [Create WhatsApp QR Connection](actions/create-whats-app-qr-connection.md) | `POST /whatsapp/channel/create` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/channel/create-whatsapp-qr-connection) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactUuid` | [docs](https://developers.2chat.co/docs/API/Contacts/delete-contact) |
| [Delete Message](actions/delete-message.md) | `DELETE /whatsapp/message/:session_key/:message_uuid` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/delete-message) |
| [Execute Channel Command](actions/execute-channel-command.md) | `POST /whatsapp/channel/:channel_uuid/:command` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/channel/execute-channel-command) |
| [Get a Message](actions/get-a-message.md) | `GET /whatsapp/message/:session_key/:message_uuid` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/get-single-message) |
| [Get Account Info](actions/get-account-info.md) | `GET /info` | [docs](https://developers.2chat.co/docs/API/authentication) |
| [Get Channel Status](actions/get-channel-status.md) | `GET /whatsapp/channel/:channel_uuid/status` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/channel/get-channel-status) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactUuid` | [docs](https://developers.2chat.co/docs/API/Contacts/get-contact) |
| [Get Messages by Phone Number](actions/get-messages-by-phone-number.md) | `GET /whatsapp/messages/:from_number/:remote_number` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/get-messages) |
| [Get WhatsApp Number](actions/get-whats-app-number.md) | `GET /whatsapp/channel/:channel_uuid` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/get-number) |
| [List All Webhooks](actions/list-all-webhooks.md) | `GET /webhooks` | [docs](https://developers.2chat.co/docs/API/Webhooks/list-all-webhooks) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.2chat.co/docs/API/Contacts/list-contacts) |
| [List Conversations](actions/list-conversations.md) | `GET /whatsapp/conversations/:channel_uuid` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/list-conversations) |
| [List Group Participants](actions/list-group-participants.md) | `GET /whatsapp/group/:group_uuid` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/list-whatsapp-group-participants) |
| [List Webhooks By Channel](actions/list-webhooks-by-channel.md) | `GET /webhooks/channel/:channel_uuid` | [docs](https://developers.2chat.co/docs/API/Webhooks/list-webhooks-by-channel) |
| [List WhatsApp Groups](actions/list-whats-app-groups.md) | `GET /whatsapp/groups/:from_number` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/list-whatsapp-groups) |
| [List WhatsApp Numbers](actions/list-whats-app-numbers.md) | `GET /whatsapp/get-numbers` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/list-numbers) |
| [Remove Participant](actions/remove-participant.md) | `POST /whatsapp/group/:group_uuid/remove-participant` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/remove-participant) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/search` | [docs](https://developers.2chat.co/docs/API/Contacts/search-contacts) |
| [Send WhatsApp Message](actions/send-whats-app-message.md) | `POST /whatsapp/send-message` | [docs](https://developers.2chat.co/docs/API/WhatsApp/Web/send-message) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contactUuid` | [docs](https://developers.2chat.co/docs/API/Contacts/update-contact) |
