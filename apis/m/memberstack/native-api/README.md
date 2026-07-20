# Memberstack: Native API Reference

A consolidated summary of Memberstack's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://developers.memberstack.com/admin-rest-api
- **API base URL:** `https://admin.memberstack.com`

## Authentication

### API Key

Authenticate with your Memberstack secret key via X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developers.memberstack.com/admin-rest-api/quick-start#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `endCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–200). Use `after` in the query string as the pagination cursor.

## Sorting

Set the sort field with `order` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Free Plan to Member](actions/add-free-plan-to-member.md) | `POST /members/:id/add-plan` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [Create Data Record](actions/create-data-record.md) | `POST /v2/data-tables/:tableKey/records` | [docs](https://developers.memberstack.com/admin-rest-api/data-tables) |
| [Create Member](actions/create-member.md) | `POST /members` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [Delete Data Record](actions/delete-data-record.md) | `DELETE /v2/data-tables/:tableKey/records/:recordId` | [docs](https://developers.memberstack.com/admin-rest-api/data-tables) |
| [Delete Member](actions/delete-member.md) | `DELETE /members/:id` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [Get Data Table](actions/get-data-table.md) | `GET /v2/data-tables/:tableKey` | [docs](https://developers.memberstack.com/admin-rest-api/data-tables) |
| [Get Member](actions/get-member.md) | `GET /members/:id_or_email` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [List Data Tables](actions/list-data-tables.md) | `GET /v2/data-tables` | [docs](https://developers.memberstack.com/admin-rest-api/data-tables) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [Query Data Records](actions/query-data-records.md) | `POST /v2/data-tables/:tableKey/records/query` | [docs](https://developers.memberstack.com/admin-rest-api/data-tables) |
| [Remove Free Plan from Member](actions/remove-free-plan-from-member.md) | `POST /members/:id/remove-plan` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [Update Data Record](actions/update-data-record.md) | `PUT /v2/data-tables/:tableKey/records/:recordId` | [docs](https://developers.memberstack.com/admin-rest-api/data-tables) |
| [Update Member](actions/update-member.md) | `PATCH /members/:id` | [docs](https://developers.memberstack.com/admin-rest-api/member-actions) |
| [Verify Member Token](actions/verify-member-token.md) | `POST /members/verify-token` | [docs](https://developers.memberstack.com/admin-rest-api/verification) |
