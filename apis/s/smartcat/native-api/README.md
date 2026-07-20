# Smartcat: Native API Reference

A consolidated summary of Smartcat's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.smartcat.com/api
- **API base URL:** `https://smartcat.ai`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.smartcat.com/api-guides/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Document](actions/add-project-document.md) | `POST /api/integration/v1/project/document` | [docs](https://developers.smartcat.com/api/#add-a-document-to-the-project) |
| [Create Project](actions/create-project.md) | `POST /api/integration/v1/project/create` | [docs](https://developers.smartcat.com/api/#create-the-project) |
| [Create Translation Memory](actions/create-translation-memory.md) | `POST /api/integration/v1/translationmemory` | [docs](https://developers.smartcat.com/api/#create-an-empty-tm) |
| [Delete Documents](actions/delete-documents.md) | `DELETE /api/integration/v1/document` | [docs](https://developers.smartcat.com/api/#delete-one-or-several-documents) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/integration/v1/project/:projectId` | [docs](https://developers.smartcat.com/api/#delete-the-project) |
| [Delete Translation Memory](actions/delete-translation-memory.md) | `DELETE /api/integration/v1/translationmemory/:tmId` | [docs](https://developers.smartcat.com/api/#delete-a-tm) |
| [Download Document Export](actions/download-document-export.md) | `GET /api/integration/v1/document/export/:taskId` | [docs](https://developers.smartcat.com/api/#download-the-export-results) |
| [Get Account](actions/get-account.md) | `GET /api/integration/v1/account` | [docs](https://developers.smartcat.com/api/#fetch-the-account-details) |
| [Get Default Glossary](actions/get-default-glossary.md) | `GET /api/integration/v1/glossaries/default` | [docs](https://developers.smartcat.com/api/#fetch-default-glossary-from-the-current-account) |
| [Get Document](actions/get-document.md) | `GET /api/integration/v1/document` | [docs](https://developers.smartcat.com/api/#fetch-the-document-details) |
| [Get Document Statistics](actions/get-document-statistics.md) | `GET /api/integration/v1/document/statistics` | [docs](https://developers.smartcat.com/api/#fetch-statistics) |
| [Get Glossary Import Task Status](actions/get-glossary-import-task-status.md) | `GET /api/integration/v1/glossary/importTaskState/:taskId` | [docs](https://developers.smartcat.com/api/#fetch-the-status-of-a-concept-import-task) |
| [Get Project](actions/get-project.md) | `GET /api/integration/v1/project/:projectId` | [docs](https://developers.smartcat.com/api/#receive-the-project-model) |
| [Get Translation Memory](actions/get-translation-memory.md) | `GET /api/integration/v1/translationmemory/:tmId` | [docs](https://developers.smartcat.com/api/#fetch-information-about-the-tm) |
| [Import Glossary](actions/import-glossary.md) | `POST /api/integration/v1/glossary/import` | [docs](https://developers.smartcat.com/api/#create-a-task-for-importing-concepts-from-a-glossary-file) |
| [List Glossaries](actions/list-glossaries.md) | `GET /api/integration/v1/glossaries` | [docs](https://developers.smartcat.com/api/#fetch-glossaries-from-the-current-account) |
| [List MT Engines](actions/list-mt-engines.md) | `GET /api/integration/v1/account/mtengines` | [docs](https://developers.smartcat.com/api/#fetch-the-list-of-mt-services-available-for-the-account) |
| [List Projects](actions/list-projects.md) | `GET /api/integration/v1/project/list` | [docs](https://developers.smartcat.com/api/#fetch-the-list-of-account-projects) |
| [List Templates](actions/list-templates.md) | `GET /api/integration/v1/template` | [docs](https://developers.smartcat.com/api/#get-all-templates-available-in-the-workspace) |
| [List Translation Memories](actions/list-translation-memories.md) | `GET /api/integration/v1/translationmemory` | [docs](https://developers.smartcat.com/api/#fetch-the-available-tms-filtered-per-account) |
| [Request Document Export](actions/request-document-export.md) | `POST /api/integration/v1/document/export` | [docs](https://developers.smartcat.com/api/#request-the-documents-export) |
| [Request Glossary Export](actions/request-glossary-export.md) | `POST /api/integration/v1/glossary/export` | [docs](https://developers.smartcat.com/api/#create-a-task-for-export-the-glossary) |
| [Update Document](actions/update-document.md) | `PUT /api/integration/v1/document/update` | [docs](https://developers.smartcat.com/api/#update-the-specified-document) |
| [Update Project](actions/update-project.md) | `PUT /api/integration/v1/project/:projectId` | [docs](https://developers.smartcat.com/api/#update-a-project-by-id) |
