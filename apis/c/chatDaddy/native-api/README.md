# ChatDaddy: Native API Reference

A consolidated summary of ChatDaddy's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://chatdaddy.stoplight.io/docs/openapi/7492869297330-getting-started-with-api
- **OpenAPI specification:** https://chatdaddy.stoplight.io/docs/openapi/7492869297330-getting-started-with-api
- **API base URL:** `https://api.chatdaddy.tech/im`

## Authentication

### Bearer API Token

Authenticate ChatDaddy IM API requests with a bearer API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://chatdaddy.stoplight.io/docs/openapi/7492869297330-getting-started-with-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `contacts`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Contact Exists](actions/check-contact-exists.md) | `GET /contacts/exists` | [docs](https://chatdaddy.stoplight.io/docs/openapi/1b1833007efdf-check-a-given-user-exists-on-the-im-platform) |
| [Close Account Connection](actions/close-account-connection.md) | `POST /accounts/{accountId}/close` | [docs](https://chatdaddy.stoplight.io/docs/openapi/2d9772dc79135-close-connection-to-the-account) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://chatdaddy.stoplight.io/docs/openapi/ae125c4f23616-add-a-new-account) |
| [Create Contacts](actions/create-contacts.md) | `POST /contacts/upsert` | [docs](https://chatdaddy.stoplight.io/docs/openapi/243d11ecc97e7-create-contacts) |
| [Create CRM Ticket](actions/create-crm-ticket.md) | `POST /crm/tickets` | [docs](https://chatdaddy.stoplight.io/docs/openapi/f662d3d411a76-create-a-new-crm-ticket) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://chatdaddy.stoplight.io/docs/openapi/5ccbb3b027800-create-a-tag) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/{accountId}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/c23e7da63b08f-enqueues-a-task-to-delete-the-account) |
| [Delete Contacts](actions/delete-contacts.md) | `DELETE /contacts` | [docs](https://chatdaddy.stoplight.io/docs/openapi/2470d0f1cdf51-delete-contacts) |
| [Delete CRM Ticket](actions/delete-crm-ticket.md) | `DELETE /crm/tickets/{id}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/26376a43d5d42-delete-a-crm-ticket) |
| [Delete Message](actions/delete-message.md) | `DELETE /messages/{accountId}/{chatId}/{id}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/cb46687acadb3-delete-a-message) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags` | [docs](https://chatdaddy.stoplight.io/docs/openapi/9d77df923356c-delete-a-tag) |
| [Get Bulk Messages](actions/get-bulk-messages.md) | `GET /messages/bulk` | [docs](https://chatdaddy.stoplight.io/docs/openapi/0f700d7748ca2-bulk-message-get) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://chatdaddy.stoplight.io/docs/openapi/9b7cad02ca629-get-the-list-of-all-accounts) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /messages/{accountId}/{chatId}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/65b9cd3fc76e9-fetch-messages-of-the-chat) |
| [List Chats](actions/list-chats.md) | `GET /chats` | [docs](https://chatdaddy.stoplight.io/docs/openapi/b6ddd4eb5d04b-get-chats) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://chatdaddy.stoplight.io/docs/openapi/6d5e4b6a5c72f-get-contacts) |
| [List CRM Boards](actions/list-crm-boards.md) | `GET /crm/boards` | [docs](https://chatdaddy.stoplight.io/docs/openapi/349d52b45fce4-get-all-crm-boards-for-the-team) |
| [List CRM Tickets](actions/list-crm-tickets.md) | `GET /crm/tickets` | [docs](https://chatdaddy.stoplight.io/docs/openapi/513fed376d8bc-get-crm-tickets) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://chatdaddy.stoplight.io/docs/openapi/46d29c27bcf74-get-all-the-tags) |
| [Open Account Connection](actions/open-account-connection.md) | `POST /accounts/{accountId}/open` | [docs](https://chatdaddy.stoplight.io/docs/openapi/b716cf29b5f5d-open-connection-to-the-account) |
| [Search Messages](actions/search-messages.md) | `GET /messages/search` | [docs](https://chatdaddy.stoplight.io/docs/openapi/c393f706dbd77-search-messages) |
| [Send Message](actions/send-message.md) | `POST /messages/{accountId}/{chatId}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/5f6bdc0458e27-send-a-message) |
| [Send Message to Chats](actions/send-message-to-chats.md) | `POST /messages` | [docs](https://chatdaddy.stoplight.io/docs/openapi/26d693d66f6eb-send-a-message-to-one-or-more-chats) |
| [Update Chat](actions/update-chat.md) | `PATCH /chats/{accountId}/{id}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/5f76fa2ed242f-update-a-chat-read-unread-archive-pin-etc) |
| [Update Chat Presence](actions/update-chat-presence.md) | `POST /chats/{accountId}/{id}/presence` | [docs](https://chatdaddy.stoplight.io/docs/openapi/60a7396ac5198-update-a-chat-s-presence) |
| [Update Contacts](actions/update-contacts.md) | `PATCH /contacts` | [docs](https://chatdaddy.stoplight.io/docs/openapi/e5072e0b9e942-update-contacts) |
| [Update CRM Ticket](actions/update-crm-ticket.md) | `PATCH /crm/tickets/{id}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/9fa1268186138-update-a-crm-ticket) |
| [Update Message](actions/update-message.md) | `PATCH /messages/{accountId}/{chatId}/{id}` | [docs](https://chatdaddy.stoplight.io/docs/openapi/d322f828da052-modify-a-message-note) |
| [Update Messages in Bulk](actions/update-messages-in-bulk.md) | `POST /messages/bulk-action` | [docs](https://chatdaddy.stoplight.io/docs/openapi/da7f880ef4d31-perform-bulk-actions-on-messages) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags` | [docs](https://chatdaddy.stoplight.io/docs/openapi/26bd392155c0c-modify-a-tag) |
