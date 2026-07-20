# Softr: Native API Reference

A consolidated summary of Softr's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.softr.io/softr-api
- **API base URL:** `https://tables-api.softr.io/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Softr Domain:** `softr_domain` · optional · Required for Softr user-management endpoints; use the published app domain or custom domain.

Send these headers with each API request:

```http
Softr-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.softr.io/softr-api/softr-database-api/authorisation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10; maximum 200). Use `offset` in the query string as the record offset.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Table Field](actions/add-table-field.md) | `POST /databases/:databaseId/tables/:tableId/fields` | [docs](https://docs.softr.io/softr-api/softr-database-api/table-fields/add-table-field) |
| [Create Database](actions/create-database.md) | `POST /databases` | [docs](https://docs.softr.io/softr-api/softr-database-api/databases/create-a-database) |
| [Create Record](actions/create-record.md) | `POST /databases/:databaseId/tables/:tableId/records` | [docs](https://docs.softr.io/softr-api/softr-database-api/records/create-record) |
| [Create Table](actions/create-table.md) | `POST /databases/:databaseId/tables` | [docs](https://docs.softr.io/softr-api/softr-database-api/tables/create-table) |
| [Create User](actions/create-user.md) | `POST https://studio-api.softr.io/v1/api/users` | [docs](https://docs.softr.io/softr-api/api-setup-and-endpoints#create-user) |
| [Delete Database](actions/delete-database.md) | `DELETE /databases/:databaseId` | [docs](https://docs.softr.io/softr-api/softr-database-api/databases/delete-database) |
| [Delete Record](actions/delete-record.md) | `DELETE /databases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://docs.softr.io/softr-api/softr-database-api/records/delete-record) |
| [Delete Table](actions/delete-table.md) | `DELETE /databases/:databaseId/tables/:tableId` | [docs](https://docs.softr.io/softr-api/softr-database-api/tables/delete-table) |
| [Delete Table Field](actions/delete-table-field.md) | `DELETE /databases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://docs.softr.io/softr-api/softr-database-api/table-fields/delete-table-field) |
| [Delete User](actions/delete-user.md) | `DELETE https://studio-api.softr.io/v1/api/users/:email` | [docs](https://docs.softr.io/softr-api/api-setup-and-endpoints#delete-user) |
| [Generate User Magic Link](actions/generate-user-magic-link.md) | `POST https://studio-api.softr.io/v1/api/users/magic-link/generate/:email` | [docs](https://docs.softr.io/softr-api/api-setup-and-endpoints#generate-a-magic-link-for-the-user) |
| [Get Database](actions/get-database.md) | `GET /databases/:databaseId` | [docs](https://docs.softr.io/softr-api/softr-database-api/databases/get-single-database) |
| [Get Record](actions/get-record.md) | `GET /databases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://docs.softr.io/softr-api/softr-database-api/records/get-single-record) |
| [Get Table](actions/get-table.md) | `GET /databases/:databaseId/tables/:tableId` | [docs](https://docs.softr.io/softr-api/softr-database-api/tables/get-single-table) |
| [Get Table Field](actions/get-table-field.md) | `GET /databases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://docs.softr.io/softr-api/softr-database-api/table-fields/get-table-field) |
| [List Databases](actions/list-databases.md) | `GET /databases` | [docs](https://docs.softr.io/softr-api/softr-database-api/databases/get-databases) |
| [List Records](actions/list-records.md) | `GET /databases/:databaseId/tables/:tableId/records` | [docs](https://docs.softr.io/softr-api/softr-database-api/records/get-records) |
| [List Table Views](actions/list-table-views.md) | `GET /databases/:databaseId/tables/:tableId/views` | [docs](https://docs.softr.io/softr-api/softr-database-api/tables/get-table-views) |
| [List Tables](actions/list-tables.md) | `GET /databases/:databaseId/tables` | [docs](https://docs.softr.io/softr-api/softr-database-api/tables/get-tables) |
| [Search Records](actions/search-records.md) | `POST /databases/:databaseId/tables/:tableId/records/search` | [docs](https://docs.softr.io/softr-api/softr-database-api/records/search-records) |
| [Sync Users](actions/sync-users.md) | `POST https://studio-api.softr.io/v1/api/users/sync` | [docs](https://docs.softr.io/softr-api/api-setup-and-endpoints#sync-a-single-user-group-of-users-or-all-users) |
| [Update Database](actions/update-database.md) | `PUT /databases/:databaseId` | [docs](https://docs.softr.io/softr-api/softr-database-api/databases/update-database) |
| [Update Record](actions/update-record.md) | `PATCH /databases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://docs.softr.io/softr-api/softr-database-api/records/update-record) |
| [Update Table](actions/update-table.md) | `PUT /databases/:databaseId/tables/:tableId` | [docs](https://docs.softr.io/softr-api/softr-database-api/tables/update-table) |
| [Update Table Field](actions/update-table-field.md) | `PUT /databases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://docs.softr.io/softr-api/softr-database-api/table-fields/update-table-field) |
| [Validate Authentication Token](actions/validate-authentication-token.md) | `POST https://priscilla41205.softr.app/v1/api/users/validate-token` | [docs](https://docs.softr.io/softr-api/api-setup-and-endpoints#validate-an-authentication-token) |
