# Ninox: Native API Reference

A consolidated summary of Ninox's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://forum.ninox.com/t/83yzlg7/introduction-to-ninox-api
- **API base URL:** `https://api.ninox.com/v1`

## Authentication

### Personal Access Token

Connect Ninox with a Personal Access Token used as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://forum.ninox.com/t/83yzlg7/introduction-to-ninox-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Update Records](actions/create-or-update-records.md) | `POST teams/:teamid/databases/:dbid/tables/:tableid/records` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Delete File](actions/delete-file.md) | `DELETE teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files/:file` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Delete Record](actions/delete-record.md) | `DELETE teams/:teamid/databases/:dbid/tables/:tableid/records/:recordid` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Delete Records](actions/delete-records.md) | `DELETE teams/:teamid/databases/:dbid/tables/:tableid/records` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Download File](actions/download-file.md) | `GET teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files/:file` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Execute Read-Only Query Via GET](actions/execute-read-only-query-via-get.md) | `GET teams/:teamId/databases/:dbId/query` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Execute Read-Only Query Via POST](actions/execute-read-only-query-via-post.md) | `POST teams/:teamId/databases/:dbId/query` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Execute Writable Query](actions/execute-writable-query.md) | `POST teams/:teamId/databases/:dbId/exec` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Find Record By POST](actions/find-record-by-post.md) | `POST teams/:teamid/databases/:dbid/tables/:tableid/record` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Database Changes](actions/get-database-changes.md) | `GET teams/:teamId/databases/:dbId/changes` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Database Schema](actions/get-database-schema.md) | `GET teams/:teamid/databases/:dbid` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files/:file/metadata` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get File Thumbnail](actions/get-file-thumbnail.md) | `GET teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files/:file/thumb.jpg` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Record](actions/get-record.md) | `GET teams/:teamid/databases/:dbid/tables/:tableid/records/:recordid` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Record Changes](actions/get-record-changes.md) | `GET teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/changes` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Table Changes](actions/get-table-changes.md) | `GET teams/:teamId/databases/:dbId/tables/:tableId/changes` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Table Schema](actions/get-table-schema.md) | `GET teams/:teamid/databases/:dbid/tables/:tableid` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Get Workspace](actions/get-workspace.md) | `GET teams/:teamid` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [List Databases](actions/list-databases.md) | `GET teams/:teamid/databases` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [List File Metadata](actions/list-file-metadata.md) | `GET teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [List Records](actions/list-records.md) | `GET teams/:teamid/databases/:dbid/tables/:tableid/records` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [List Tables](actions/list-tables.md) | `GET teams/:teamid/databases/:dbid/tables` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [List Workspaces](actions/list-workspaces.md) | `GET teams` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Update Record](actions/update-record.md) | `PUT teams/:teamid/databases/:dbid/tables/:tableid/records/:recordid` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
| [Upload File](actions/upload-file.md) | `POST teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files` | [docs](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud) |
