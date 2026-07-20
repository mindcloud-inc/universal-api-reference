# smapOne: Native API Reference

A consolidated summary of smapOne's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://platform.smapone.com/swagger
- **OpenAPI specification:** https://platform.smapone.com/swagger/result/v1_Web.json
- **API base URL:** `https://platform.smapone.com/Backend`

## Authentication

### API Key

Authenticate smapOne REST API requests with the Creator API token/access token as the accessToken query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://faq.smapone.com/kb/guide/en/how-do-i-authenticate-to-the-rest-api-KBRVL03Rip/Steps/966447)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create task](actions/create-task.md) | `POST /preview/Smaps/{smapId}/Versions/{version}/Tasks` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Delete record](actions/delete-record.md) | `DELETE /v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Delete records](actions/delete-records.md) | `DELETE /v1/Smaps/{smapId}/Versions/{version}/Data` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get account](actions/get-account.md) | `GET /intern/Account` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get account stats](actions/get-account-stats.md) | `GET /intern/Account/Stats` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get category smaps](actions/get-category-smaps.md) | `GET /smaps/overview/categories/{categoryId}` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get datasource](actions/get-datasource.md) | `GET /intern/DataSource/{dataSourceId}` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get datasource values](actions/get-datasource-values.md) | `GET /intern/DataSource/{dataSourceId}/Versions/{dataSourceVersion}/Definition/Values` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get record](actions/get-record.md) | `GET /v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get record file](actions/get-record-file.md) | `GET /v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}/Files/{fileId}` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get smap](actions/get-smap.md) | `GET /v1/Smaps/{smapId}` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Get smap categories](actions/get-smap-categories.md) | `GET /smaps/overview/{smapId}/categories` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List categories](actions/list-categories.md) | `GET /smaps/overview/categories` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List datasource versions](actions/list-datasource-versions.md) | `GET /intern/DataSource/{dataSourceId}/Versions` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List datasources](actions/list-datasources.md) | `GET /intern/DataSource` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List record files](actions/list-record-files.md) | `GET /v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}/Files` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List records](actions/list-records.md) | `GET /v1/Smaps/{smapId}/Versions/{version}/Data` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List smap overview](actions/list-smap-overview.md) | `GET /smaps/overview` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List smap versions](actions/list-smap-versions.md) | `GET /v1/Smaps/{smapId}/Versions` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List smaps](actions/list-smaps.md) | `GET /v1/Smaps` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List templates](actions/list-templates.md) | `GET /intern/Templates/Smaps` | [docs](https://platform.smapone.com/swagger/index.html) |
| [List users](actions/list-users.md) | `GET /intern/Users` | [docs](https://platform.smapone.com/swagger/index.html) |
| [Update task state](actions/update-task-state.md) | `PUT /preview/Smaps/{smapId}/Versions/{version}/Tasks/{taskId}/State` | [docs](https://platform.smapone.com/swagger/index.html) |
