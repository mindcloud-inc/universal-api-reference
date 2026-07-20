# Pinecone: Native API Reference

A consolidated summary of Pinecone's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.pinecone.io/reference/api/introduction
- **API base URL:** `https://api.pinecone.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Index Name:** `indexName` · required · The Pinecone index name to use for index-level actions.
- **Index Host:** `indexHost` · required · The Pinecone index host used for data-plane operations.

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.pinecone.io/reference/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `paginationToken` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Configure Index](actions/configure-index.md) | `PATCH /indexes/:index_name` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/configure_index) |
| [Create Backup](actions/create-backup.md) | `POST /indexes/:index_name/backups` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_backup) |
| [Create Index](actions/create-index.md) | `POST /indexes` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_index) |
| [Create Index From Backup](actions/create-index-from-backup.md) | `POST /backups/:backup_id/create-index` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_index_from_backup) |
| [Create Index With Integrated Embedding](actions/create-index-with-integrated-embedding.md) | `POST /indexes/create-for-model` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_for_model) |
| [Create Namespace](actions/create-namespace.md) | `POST {{credentials.indexHost}}/namespaces` | [docs](https://docs.pinecone.io/reference/api/2025-10/data-plane/createnamespace) |
| [Delete Backup](actions/delete-backup.md) | `DELETE /backups/:backup_id` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/delete_backup) |
| [Delete Namespace](actions/delete-namespace.md) | `DELETE {{credentials.indexHost}}/namespaces/:namespace` | [docs](https://docs.pinecone.io/reference/api/2025-10/data-plane/deletenamespace) |
| [Describe Backup](actions/describe-backup.md) | `GET /backups/:backup_id` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/describe_backup) |
| [Describe Index](actions/describe-index.md) | `GET /indexes/:index_name` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/describe_index) |
| [Describe Model](actions/describe-model.md) | `GET /models/:model_name` | [docs](https://docs.pinecone.io/reference/api/2025-10/inference/describe_model) |
| [Describe Namespace](actions/describe-namespace.md) | `GET {{credentials.indexHost}}/namespaces/:namespace` | [docs](https://docs.pinecone.io/reference/api/2025-10/data-plane/describenamespace) |
| [Describe Restore Job](actions/describe-restore-job.md) | `GET /restore-jobs/:job_id` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/describe_restore_job) |
| [Generate Vectors](actions/generate-vectors.md) | `POST /embed` | [docs](https://docs.pinecone.io/reference/api/2025-10/inference/generate-embeddings) |
| [Get Index Stats](actions/get-index-stats.md) | `POST {{credentials.indexHost}}/describe_index_stats` | [docs](https://docs.pinecone.io/reference/api/2025-10/data-plane/describeindexstats) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/list_collections) |
| [List Imports](actions/list-imports.md) | `GET {{credentials.indexHost}}/bulk/imports` | [docs](https://docs.pinecone.io/reference/api/2025-10/data-plane/list_imports) |
| [List Index Backups](actions/list-index-backups.md) | `GET /indexes/:index_name/backups` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/list_index_backups) |
| [List Indexes](actions/list-indexes.md) | `GET /indexes` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/list_indexes) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://docs.pinecone.io/reference/api/2025-10/inference/list_models) |
| [List Namespaces](actions/list-namespaces.md) | `GET {{credentials.indexHost}}/namespaces` | [docs](https://docs.pinecone.io/reference/api/2025-10/data-plane/listnamespaces) |
| [List Project Backups](actions/list-project-backups.md) | `GET /backups` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/list_project_backups) |
| [List Restore Jobs](actions/list-restore-jobs.md) | `GET /restore-jobs` | [docs](https://docs.pinecone.io/reference/api/2025-10/control-plane/list_restore_jobs) |
| [Rerank Results](actions/rerank-results.md) | `POST /rerank` | [docs](https://docs.pinecone.io/reference/api/2025-10/inference/rerank) |
