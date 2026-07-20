# Grist: Native API Reference

A consolidated summary of Grist's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://support.getgrist.com/api/
- **API base URL:** `https://docs.getgrist.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.getgrist.com/api/#api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100).

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Columns](actions/add-columns.md) | `POST /docs/:docId/tables/:tableId/columns` | [docs](https://support.getgrist.com/api/#tag/columns/operation/addColumns) |
| [Add Records](actions/add-records.md) | `POST /docs/:docId/tables/:tableId/records` | [docs](https://support.getgrist.com/api/#tag/records/operation/addRecords) |
| [Add Tables](actions/add-tables.md) | `POST /docs/:docId/tables` | [docs](https://support.getgrist.com/api/#tag/tables/operation/addTables) |
| [Create Document](actions/create-document.md) | `POST /workspaces/:workspaceId/docs` | [docs](https://support.getgrist.com/api/#tag/docs/operation/createDoc) |
| [Create Webhook](actions/create-webhook.md) | `POST /docs/:docId/webhooks` | [docs](https://support.getgrist.com/api/#tag/webhooks/operation/createWebhooks) |
| [Delete Column](actions/delete-column.md) | `DELETE /docs/:docId/tables/:tableId/columns/:colId` | [docs](https://support.getgrist.com/api/#tag/columns/operation/deleteColumn) |
| [Delete Document](actions/delete-document.md) | `DELETE /docs/:docId` | [docs](https://support.getgrist.com/api/#tag/docs/operation/deleteDoc) |
| [Delete Records](actions/delete-records.md) | `POST /docs/:docId/tables/:tableId/records/delete` | [docs](https://support.getgrist.com/api/#tag/records/operation/deleteRecords) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /docs/:docId/webhooks/:webhookId` | [docs](https://support.getgrist.com/api/#tag/webhooks/operation/deleteWebhook) |
| [Get Document](actions/get-document.md) | `GET /docs/:docId` | [docs](https://support.getgrist.com/api/#tag/docs/operation/describeDoc) |
| [Get Organization](actions/get-organization.md) | `GET /orgs/:orgId` | [docs](https://support.getgrist.com/api/#tag/orgs/operation/describeOrg) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://support.getgrist.com/api/#tag/workspaces/operation/describeWorkspace) |
| [List Columns](actions/list-columns.md) | `GET /docs/:docId/tables/:tableId/columns` | [docs](https://support.getgrist.com/api/#tag/columns/operation/listColumns) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://support.getgrist.com/api/#tag/orgs/operation/listOrgs) |
| [List Records](actions/list-records.md) | `GET /docs/:docId/tables/:tableId/records` | [docs](https://support.getgrist.com/api/#tag/records/operation/listRecords) |
| [List Tables](actions/list-tables.md) | `GET /docs/:docId/tables` | [docs](https://support.getgrist.com/api/#tag/tables/operation/listTables) |
| [List Webhooks](actions/list-webhooks.md) | `GET /docs/:docId/webhooks` | [docs](https://support.getgrist.com/api/#tag/webhooks/operation/listWebhooks) |
| [List Workspaces](actions/list-workspaces.md) | `GET /orgs/:orgId/workspaces` | [docs](https://support.getgrist.com/api/#tag/workspaces/operation/listWorkspaces) |
| [Replace Columns](actions/replace-columns.md) | `PUT /docs/:docId/tables/:tableId/columns` | [docs](https://support.getgrist.com/api/#tag/columns/operation/replaceColumns) |
| [Replace Records](actions/replace-records.md) | `PUT /docs/:docId/tables/:tableId/records` | [docs](https://support.getgrist.com/api/#tag/records/operation/replaceRecords) |
| [Run SQL Query](actions/run-sql-query.md) | `POST /docs/:docId/sql` | [docs](https://support.getgrist.com/api/#tag/sql/operation/runSql) |
| [Update Records](actions/update-records.md) | `PATCH /docs/:docId/tables/:tableId/records` | [docs](https://support.getgrist.com/api/#tag/records/operation/modifyRecords) |
| [Update Tables](actions/update-tables.md) | `PATCH /docs/:docId/tables` | [docs](https://support.getgrist.com/api/#tag/tables/operation/modifyTables) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /docs/:docId/webhooks/:webhookId` | [docs](https://support.getgrist.com/api/#tag/webhooks/operation/modifyWebhook) |
