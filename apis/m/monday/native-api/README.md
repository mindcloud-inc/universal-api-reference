# Monday: Native API Reference

A consolidated summary of Monday's API configuration and 20 documented operations.

- **API base URL:** `https://api.monday.com/v2/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the request parameters to set the page size (default 25; accepted range 1–500). Use `cursor` in the request parameters as the pagination cursor.

## Endpoints (20 documented)

| Operation | Method & path |
| --- | --- |
| [Create Item](actions/create-item.md) | `POST` |
| [Create Sub Item](actions/create-sub-item.md) | `POST` |
| [Create Update Record](actions/create-update-record.md) | `POST` |
| [Delete Update Record](actions/delete-update-record.md) | `POST` |
| [Get All SubItems Of Of an Item by Item's Column Value](actions/get-all-sub-items-of-of-an-item-by-items-column-value.md) | `POST` |
| [Get Board By Id](actions/get-board-by-id.md) | `POST` |
| [Get Board Items](actions/get-board-items.md) | `POST` |
| [Get Board Items by Column Value](actions/get-board-items-by-column-value.md) | `POST` |
| [Get Board Items with Sub Items](actions/get-board-items-sub-items.md) | `POST` |
| [Get Boards](actions/get-boards.md) | `POST` |
| [Get Boards With items](actions/get-boards-with-items.md) | `POST` |
| [Get Boards With items (GraphQL)](actions/get-boards-with-items-graph-ql.md) | `POST` |
| [Get Columns](actions/get-columns.md) | `POST` |
| [Get Item Details](actions/get-item-details.md) | `POST` |
| [Get Item Details with Connect Board Item ID's](actions/get-item-details-with-connect-board-item-i-ds.md) | `POST` |
| [Search In Board With Item Name](actions/search-in-board-with-item-name.md) | `POST` |
| [Send Notifications](actions/send-notifications.md) | `POST` |
| [Update Multiple Column Values](actions/update-multiple-column-values.md) | `POST` |
| [Update Payment Status](actions/update-payment-status.md) | `POST` |
| [Update Payment Status Sub-Item](actions/update-payment-status-sub-item.md) | `POST` |
