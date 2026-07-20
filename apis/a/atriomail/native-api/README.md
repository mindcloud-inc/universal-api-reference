# Atriomail: Native API Reference

A consolidated summary of Atriomail's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://system.atriomail.com/api/documentation
- **API base URL:** `https://system.atriomail.com/api/v1`

## Authentication

### API Key

Authenticate AtrioMail API requests with an API key sent in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://system.atriomail.com/api/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 15; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | `POST /domains` | [docs](https://system.atriomail.com/api/documentation) |
| [Create Mailbox](actions/create-mailbox.md) | `POST /mailboxes` | [docs](https://system.atriomail.com/api/documentation) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://system.atriomail.com/api/documentation) |
| [Delete Mailbox](actions/delete-mailbox.md) | `DELETE /mailboxes/:mailboxId` | [docs](https://system.atriomail.com/api/documentation) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:userId` | [docs](https://system.atriomail.com/api/documentation) |
| [Get Catch-All](actions/get-catch-all.md) | `GET /catch-all/:catchAllId` |  |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://system.atriomail.com/api/documentation) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domainId` | [docs](https://system.atriomail.com/api/documentation) |
| [Get Forwarder](actions/get-forwarder.md) | `GET /forwarders/:forwarderId` |  |
| [Get Mailbox](actions/get-mailbox.md) | `GET /mailboxes/:mailboxId` | [docs](https://system.atriomail.com/api/documentation) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://system.atriomail.com/api/documentation) |
| [List Catch-Alls](actions/list-catch-alls.md) | `GET /catch-all` | [docs](https://system.atriomail.com/api/documentation) |
| [List Domain Mailboxes](actions/list-domain-mailboxes.md) | `GET /mailboxes` |  |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://system.atriomail.com/api/documentation) |
| [List Forwarders](actions/list-forwarders.md) | `GET /forwarders` | [docs](https://system.atriomail.com/api/documentation) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /mailboxes` | [docs](https://system.atriomail.com/api/documentation) |
| [List Migrations](actions/list-migrations.md) | `GET /migrations` | [docs](https://system.atriomail.com/api/documentation) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://system.atriomail.com/api/documentation) |
| [Update Mailbox](actions/update-mailbox.md) | `PUT /mailboxes/:mailboxId` | [docs](https://system.atriomail.com/api/documentation) |
| [Update User](actions/update-user.md) | `PUT /users/:userId` | [docs](https://system.atriomail.com/api/documentation) |
