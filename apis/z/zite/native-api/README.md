# Zite: Native API Reference

A consolidated summary of Zite's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://fillout.com/help/database/api
- **API base URL:** `https://tables.fillout.com/api/v1`

## Authentication

### API Key

Connect with a Fillout API key for Zite Database access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.fillout.com/help/database/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | `POST /bases` | [docs](https://fillout.com/help/database/create-database) |
| [Create Field](actions/create-field.md) | `POST /bases/:databaseId/tables/:tableId/fields` | [docs](https://fillout.com/help/database/create-field) |
| [Create Record](actions/create-record.md) | `POST /bases/:databaseId/tables/:tableId/records` | [docs](https://fillout.com/help/database/create-record) |
| [Create Table](actions/create-table.md) | `POST /bases/:databaseId/tables` | [docs](https://fillout.com/help/database/create-table) |
| [Create Webhook](actions/create-webhook.md) | `POST /bases/:databaseId/webhooks` | [docs](https://fillout.com/help/database/create-webhook) |
| [Delete Database](actions/delete-database.md) | `DELETE /bases/:databaseId` | [docs](https://fillout.com/help/database/delete-database) |
| [Delete Field](actions/delete-field.md) | `DELETE /bases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://fillout.com/help/database/delete-field) |
| [Delete Record](actions/delete-record.md) | `DELETE /bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://fillout.com/help/database/delete-record) |
| [Delete Table](actions/delete-table.md) | `DELETE /bases/:databaseId/tables/:tableId` | [docs](https://fillout.com/help/database/delete-table) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /bases/:databaseId/webhooks/:webhookId` | [docs](https://fillout.com/help/database/delete-webhook) |
| [Get Database by ID](actions/get-database-by-id.md) | `GET /bases/:databaseId` | [docs](https://fillout.com/help/database/get-database-by-id) |
| [Get Databases](actions/get-databases.md) | `GET /bases` | [docs](https://fillout.com/help/database/get-databases) |
| [Get Record by ID](actions/get-record-by-id.md) | `GET /bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://fillout.com/help/database/get-record-by-id) |
| [List Records](actions/list-records.md) | `POST /bases/:databaseId/tables/:tableId/records/list` | [docs](https://fillout.com/help/database/list-records) |
| [List Webhooks](actions/list-webhooks.md) | `GET /bases/:databaseId/webhooks` | [docs](https://fillout.com/help/database/list-webhooks) |
| [Update Field](actions/update-field.md) | `PATCH /bases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://fillout.com/help/database/update-field) |
| [Update Record](actions/update-record.md) | `PATCH /bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://fillout.com/help/database/update-record) |
| [Update Table](actions/update-table.md) | `PATCH /bases/:databaseId/tables/:tableId` | [docs](https://fillout.com/help/database/update-table) |
