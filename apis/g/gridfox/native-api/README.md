# Gridfox: Native API Reference

A consolidated summary of Gridfox's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://api.gridfox.com/swagger/index.html
- **OpenAPI specification:** https://api.gridfox.com/swagger/v1/swagger.json
- **API base URL:** `https://api.gridfox.com/`

## Authentication

### Gridfox API Key

Authenticate with a Gridfox public API key generated from the target project integrations page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
gridfox-api-key: <apiKey>
```

[Official authentication documentation](https://app.gridfox.com/apps/935a5980-5198-4439-4b9e-08de8fe02e25/integrations)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User](actions/add-user.md) | `POST /users` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Create Record](actions/create-record.md) | `POST /data/:tableName` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Delete Field File](actions/delete-field-file.md) | `DELETE /data/:tableName/:referenceFieldValue/:fieldName/:fileName` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Delete Record](actions/delete-record.md) | `DELETE /data/:tableName/:referenceFieldValue` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Download Field File](actions/download-field-file.md) | `GET /data/:tableName/:referenceFieldValue/:fieldName/:fileName` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Get Permissions](actions/get-permissions.md) | `GET /permissions` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Get Record](actions/get-record.md) | `GET /data/:tableName/:referenceFieldValue` | [docs](https://api.gridfox.com/swagger/index.html) |
| [List Record Audits](actions/list-record-audits.md) | `GET /data/:tableName/:referenceFieldValue/audit` | [docs](https://api.gridfox.com/swagger/index.html) |
| [List Tables](actions/list-tables.md) | `GET /tables` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Remove User](actions/remove-user.md) | `DELETE /users/:userId` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Search Records](actions/search-records.md) | `GET /data/:tableName` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Search User Groups](actions/search-user-groups.md) | `GET /groups` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Update Record](actions/update-record.md) | `PUT /data/:tableName/:referenceFieldValue` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Update User Group](actions/update-user-group.md) | `PUT /users/:userId` | [docs](https://api.gridfox.com/swagger/index.html) |
| [Upload Field Files](actions/upload-field-files.md) | `POST /data/:tableName/:referenceFieldValue/:fieldName` | [docs](https://api.gridfox.com/swagger/index.html) |
