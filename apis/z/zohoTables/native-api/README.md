# Zoho Tables: Native API Reference

A consolidated summary of Zoho Tables's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://tables.zoho.com/help/api/v1
- **API base URL:** `https://tables.zoho.com/api/v1`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoTables.portals.READ,ZohoTables.workspaces.READ,ZohoTables.workspaces.CREATE,ZohoTables.bases.READ,ZohoTables.bases.CREATE,ZohoTables.bases.UPDATE,ZohoTables.bases.DELETE,ZohoTables.tables.READ,ZohoTables.tables.CREATE,ZohoTables.tables.UPDATE,ZohoTables.tables.DELETE,ZohoTables.views.READ,ZohoTables.fields.READ,ZohoTables.fields.CREATE,ZohoTables.fields.UPDATE,ZohoTables.fields.DELETE,ZohoTables.records.READ,ZohoTables.records.CREATE,ZohoTables.records.UPDATE,ZohoTables.records.DELETE,ZohoTables.webhooks.UPDATE,ZohoTables.webhooks.DELETE,WorkDrive.team.ALL,WorkDrive.workspace.ALL,WorkDrive.files.ALL,ZohoCliq.webhooks.CREATE,ZohoFiles.files.ALL`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://tables.zoho.com/help/api/v1)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Base](actions/create-base.md) | `POST /bases` | [docs](https://tables.zoho.com/help/api/v1#BASES-Create-Base) |
| [Create Field](actions/create-field.md) | `POST /fields` | [docs](https://tables.zoho.com/help/api/v1#FIELDS-Create-Field) |
| [Create Record](actions/create-record.md) | `POST /records` | [docs](https://tables.zoho.com/help/api/v1#RECORDS-Create-Record-with-Data) |
| [Create Table](actions/create-table.md) | `POST /tables` | [docs](https://tables.zoho.com/help/api/v1#TABLES-Create-Table) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://tables.zoho.com/help/api/v1#WORKSPACES-Create-Workspace) |
| [Delete Base](actions/delete-base.md) | `DELETE /bases` | [docs](https://tables.zoho.com/help/api/v1#BASES-Delete-Base) |
| [Delete Field](actions/delete-field.md) | `DELETE /fields` | [docs](https://tables.zoho.com/help/api/v1#FIELDS-Delete-Field) |
| [Delete Record](actions/delete-record.md) | `DELETE /records` | [docs](https://tables.zoho.com/help/api/v1#RECORDS-Delete-Record) |
| [Delete Table](actions/delete-table.md) | `DELETE /tables` | [docs](https://tables.zoho.com/help/api/v1#TABLES-Delete-Table) |
| [Duplicate Base](actions/duplicate-base.md) | `POST /bases` | [docs](https://tables.zoho.com/help/api/v1#BASES-Duplicate-Base) |
| [Duplicate Table](actions/duplicate-table.md) | `POST /tables` | [docs](https://tables.zoho.com/help/api/v1#TABLES-Duplicate-Table) |
| [Fetch Records with Criteria](actions/fetch-records-with-criteria.md) | `POST /fetchRecordsWithCriteria` | [docs](https://tables.zoho.com/help/api/v1#RECORDS-Fetch-Record-with-Criteria) |
| [List Base](actions/list-base.md) | `GET /bases` | [docs](https://tables.zoho.com/help/api/v1#BASES-List-Bases) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://tables.zoho.com/help/api/v1#FIELDS-List-Fields) |
| [List Portals](actions/list-portals.md) | `GET /portals` | [docs](https://tables.zoho.com/help/api/v1#PORTALS-List-Portals) |
| [List Records](actions/list-records.md) | `GET /records` | [docs](https://tables.zoho.com/help/api/v1#DATA-List-Data) |
| [List Tables](actions/list-tables.md) | `GET /tables` | [docs](https://tables.zoho.com/help/api/v1#TABLES-List-Tables) |
| [List Views](actions/list-views.md) | `GET /views` | [docs](https://tables.zoho.com/help/api/v1#VIEWS-List-Views) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://tables.zoho.com/help/api/v1#WORKSPACES-List-Workspaces) |
| [Search Bases](actions/search-bases.md) | `GET /searchBases` | [docs](https://tables.zoho.com/help/api/v1#BASES-Search-Bases) |
| [Update Base](actions/update-base.md) | `PUT /bases` | [docs](https://tables.zoho.com/help/api/v1#BASES-Update-Base) |
| [Update Field](actions/update-field.md) | `PUT /fields` | [docs](https://tables.zoho.com/help/api/v1#FIELDS-Update-Field) |
| [Update Records](actions/update-records.md) | `PUT /records` | [docs](https://tables.zoho.com/help/api/v1#RECORDS-Update-Record-with-Criteria) |
| [Update Table](actions/update-table.md) | `PUT /tables` | [docs](https://tables.zoho.com/help/api/v1#TABLES-Update-Table) |
