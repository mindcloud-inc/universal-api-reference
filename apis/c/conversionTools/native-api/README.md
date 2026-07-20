# Conversion Tools: Native API Reference

A consolidated summary of Conversion Tools's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://conversiontools.io/api-documentation
- **OpenAPI specification:** https://api.conversiontools.io/openapi.yaml
- **API base URL:** `https://api.conversiontools.io/v1`

## Authentication

### API Token

Connect with your Conversion Tools API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://conversiontools.io/api-documentation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conversion Task](actions/create-conversion-task.md) | `POST /tasks` | [docs](https://conversiontools.io/api-documentation#run-conversion-task) |
| [Delete Task Files Immediately](actions/delete-task-files-immediately.md) | `POST /tasks/:taskId/delete` | [docs](https://api.conversiontools.io/openapi.yaml) |
| [Download File](actions/download-file.md) | `GET /files/:fileId` | [docs](https://conversiontools.io/api-documentation#download-result-file) |
| [Get API Configuration](actions/get-api-configuration.md) | `GET /config` | [docs](https://api.conversiontools.io/openapi.yaml) |
| [Get Authenticated User Info](actions/get-authenticated-user-info.md) | `GET /auth` | [docs](https://api.conversiontools.io/openapi.yaml) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /files/:fileId/info` | [docs](https://api.conversiontools.io/openapi.yaml) |
| [Get Task Status](actions/get-task-status.md) | `GET /tasks/:taskId` | [docs](https://conversiontools.io/api-documentation#get-task-status) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://api.conversiontools.io/openapi.yaml) |
| [Update Task Retention](actions/update-task-retention.md) | `PATCH /tasks/:taskId/retention` | [docs](https://api.conversiontools.io/openapi.yaml) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://conversiontools.io/api-documentation#upload-file-to-server) |
