# Quickbase: Native API Reference

A consolidated summary of Quickbase's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.quickbase.com/
- **API base URL:** `https://api.quickbase.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Realm Hostname:** `realmHostname` · required · Your Quickbase realm hostname, for example example.quickbase.com.

Send these headers with each API request:

```http
QB-Realm-Hostname: <realmHostname>
```

[Official authentication documentation](https://help.quickbase.com/docs/create-and-use-user-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create a Field](actions/create-a-field.md) | `POST v1/fields` | [docs](https://developer.quickbase.com/operation/createField) |
| [Create a Table](actions/create-a-table.md) | `POST v1/tables` | [docs](https://developer.quickbase.com/operation/createTable) |
| [Delete a Table](actions/delete-a-table.md) | `DELETE v1/tables/:tableId` | [docs](https://developer.quickbase.com/operation/deleteTable) |
| [Delete Field(s)](actions/delete-fields.md) | `DELETE v1/fields` | [docs](https://developer.quickbase.com/operation/deleteFields) |
| [Delete Record(s)](actions/delete-records.md) | `DELETE v1/records` | [docs](https://developer.quickbase.com/operation/deleteRecords) |
| [Get a Report](actions/get-a-report.md) | `GET v1/reports/:reportId` | [docs](https://developer.quickbase.com/operation/getReport) |
| [Get a Table](actions/get-a-table.md) | `GET v1/tables/:tableId` | [docs](https://developer.quickbase.com/operation/getTable) |
| [Get App](actions/get-app.md) | `GET v1/apps/:appId` | [docs](https://developer.quickbase.com/operation/getApp) |
| [Get Field](actions/get-field.md) | `GET v1/fields/:fieldId` | [docs](https://developer.quickbase.com/operation/getField) |
| [Get Fields for a Table](actions/get-fields-for-a-table.md) | `GET v1/fields` | [docs](https://developer.quickbase.com/operation/getFields) |
| [Get Records Modified Since](actions/get-records-modified-since.md) | `POST v1/records/modifiedSince` | [docs](https://developer.quickbase.com/operation/recordsModifiedSince) |
| [Get Reports for a Table](actions/get-reports-for-a-table.md) | `GET v1/reports` | [docs](https://developer.quickbase.com/operation/getTableReports) |
| [Get Roles](actions/get-roles.md) | `GET v1/apps/:appId/roles` | [docs](https://developer.quickbase.com/operation/getRoles) |
| [Get Tables for an App](actions/get-tables-for-an-app.md) | `GET v1/tables` | [docs](https://developer.quickbase.com/operation/getAppTables) |
| [Insert/Update Record(s)](actions/insert-update-records.md) | `POST v1/records` | [docs](https://developer.quickbase.com/operation/upsert) |
| [Query for Data](actions/query-for-data.md) | `POST v1/records/query` | [docs](https://developer.quickbase.com/operation/runQuery) |
| [Run a Formula](actions/run-a-formula.md) | `POST v1/formula/run` | [docs](https://developer.quickbase.com/operation/runFormula) |
| [Run a Report](actions/run-a-report.md) | `POST v1/reports/:reportId/run` | [docs](https://developer.quickbase.com/operation/runReport) |
| [Update a Field](actions/update-a-field.md) | `POST v1/fields/:fieldId` | [docs](https://developer.quickbase.com/operation/updateField) |
| [Update a Table](actions/update-a-table.md) | `POST v1/tables/:tableId` | [docs](https://developer.quickbase.com/operation/updateTable) |
