# Listrak Email: Native API Reference

A consolidated summary of Listrak Email's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://api.listrak.com/email
- **OpenAPI specification:** https://api.listrak.com/email/swagger/docs/v1
- **API base URL:** `https://api.listrak.com/email`

## Authentication

### Access Token

### Credentials

- **Client ID:** `clientID` · optional
- **Client Secret:** `clientSecret` · optional

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 1000; accepted range 10–5000). Use `cursor` in the query string as the pagination cursor; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get List](actions/get-list.md) | `GET /v1/List/:listID` | [docs](https://api.listrak.com/email#tag/List) |
| [Get Message](actions/get-message.md) | `GET /v1/List/:listID/Message/:messageID` | [docs](https://api.listrak.com/email#tag/List) |
| [Get Transactional Message](actions/get-transactional-message.md) | `GET /v1/List/:listID/TransactionalMessage/:messageID` | [docs](https://api.listrak.com/email#tag/List) |
| [List Messages](actions/list-messages.md) | `GET /v1/List/:listID/Message` | [docs](https://api.listrak.com/email#tag/List) |
| [List Transactional Messages](actions/list-transactional-messages.md) | `GET /v1/List/:listID/TransactionalMessage` | [docs](https://api.listrak.com/email#tag/List) |
| [List Lists](actions/new-action1.md) | `GET /v1/List` | [docs](https://api.listrak.com/email#tag/List) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /v1/List/:listId/TransactionalMessage/:transactionalMessageId/Message` | [docs](https://api.listrak.com/email#operation/TransactionalMessage_PostTransactionalMessageSend) |
