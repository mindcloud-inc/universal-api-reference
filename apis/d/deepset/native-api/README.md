# Deepset: Native API Reference

A consolidated summary of Deepset's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloud.deepset.ai/docs/api/
- **API base URL:** `https://api.cloud.deepset.ai`

## Authentication

### API Key

Use a deepset Haystack Enterprise Platform API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cloud.deepset.ai/docs/generate-api-key)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chat](actions/chat.md) | `POST /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/chat` | [docs](https://docs.cloud.deepset.ai/docs/api/main/chat-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-chat-post) |
| [Count Documents](actions/count-documents.md) | `GET /api/v1/workspaces/:workspace_name/indexes/:index_name/documents/count` | [docs](https://docs.cloud.deepset.ai/docs/api/main/count-documents-api-v-1-workspaces-workspace-name-indexes-index-name-documents-count-get) |
| [Get Document](actions/get-document.md) | `GET /api/v1/workspaces/:workspace_name/indexes/:index_name/documents/:document_id` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-document-api-v-1-workspaces-workspace-name-indexes-index-name-documents-document-id-get) |
| [Get File](actions/get-file.md) | `GET /api/v1/workspaces/:workspace_name/files/:file_id` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-file-api-v-1-workspaces-workspace-name-files-file-id-get) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /api/v1/workspaces/:workspace_name/files/:file_id/meta` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-file-meta-api-v-1-workspaces-workspace-name-files-file-id-meta-get) |
| [Get Index By Name](actions/get-index-by-name.md) | `GET /api/v1/workspaces/:workspace_name/indexes/:index_name` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-index-by-name-api-v-1-workspaces-workspace-name-indexes-index-name-get) |
| [Get Job](actions/get-job.md) | `GET /api/v2/workspaces/:workspace_id/jobs/:job_id` | [docs](https://docs.cloud.deepset.ai/docs/api/jobs/get-job-api-v-2-workspaces-workspace-id-jobs-job-id-get) |
| [Get Jobs](actions/get-jobs.md) | `GET /api/v2/workspaces/:workspace_id/jobs` | [docs](https://docs.cloud.deepset.ai/docs/api/jobs/get-jobs-api-v-2-workspaces-workspace-id-jobs-get) |
| [Get Organization](actions/get-organization.md) | `GET /api/v1/organization` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-organization-api-v-1-organization-get) |
| [Get Permissions](actions/get-permissions.md) | `GET /api/v1/organization/permissions` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-permissions-api-v-1-organization-permissions-get) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-get) |
| [Get Pipeline Issues](actions/get-pipeline-issues.md) | `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/issues` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-issues-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-issues-get) |
| [Get Pipeline Logs](actions/get-pipeline-logs.md) | `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/logs` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-logs-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-logs-get) |
| [Get Pipeline Stats](actions/get-pipeline-stats.md) | `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/stats` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-stats-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-stats-get) |
| [Get Pipeline Visualization](actions/get-pipeline-visualization.md) | `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/visualization` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-visualization-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-visualization-get) |
| [Get Pipeline YAML Configs](actions/get-pipeline-yaml-configs.md) | `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/yaml` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-yaml-configs-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-yaml-get) |
| [Get Query Set](actions/get-query-set.md) | `GET /api/v2/workspaces/:workspace_id/query_sets/:query_set_id` | [docs](https://docs.cloud.deepset.ai/docs/api/jobs/get-query-set-api-v-2-workspaces-workspace-id-query-sets-query-set-id-get) |
| [Get Query Sets](actions/get-query-sets.md) | `GET /api/v2/workspaces/:workspace_id/query_sets` | [docs](https://docs.cloud.deepset.ai/docs/api/jobs/get-query-sets-api-v-2-workspaces-workspace-id-query-sets-get) |
| [Get Roles](actions/get-roles.md) | `GET /api/v1/organization/:organization_id/roles` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-roles-api-v-1-organization-organization-id-roles-get) |
| [Get Search Sessions](actions/get-search-sessions.md) | `GET /api/v1/workspaces/:workspace_name/search_sessions` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-search-sessions-api-v-1-workspaces-workspace-name-search-sessions-get) |
| [Get Shared Job](actions/get-shared-job.md) | `GET /api/v2/workspaces/:workspace_id/shared_jobs/:shared_job_id` | [docs](https://docs.cloud.deepset.ai/docs/api/jobs/get-shared-job-api-v-2-workspaces-workspace-id-shared-jobs-shared-job-id-get) |
| [Get Shared Jobs](actions/get-shared-jobs.md) | `GET /api/v2/workspaces/:workspace_id/shared_jobs` | [docs](https://docs.cloud.deepset.ai/docs/api/jobs/get-shared-jobs-api-v-2-workspaces-workspace-id-shared-jobs-get) |
| [Get User](actions/get-user.md) | `GET /api/v1/users/:user_id` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-user-api-v-1-users-user-id-get) |
| [Get Users](actions/get-users.md) | `GET /api/v1/users` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-users-api-v-1-users-get) |
| [Get Workspace By Name](actions/get-workspace-by-name.md) | `GET /api/v1/workspaces/:workspace_name` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-workspace-by-name-api-v-1-workspaces-workspace-name-get) |
| [Health](actions/health.md) | `GET /health` | [docs](https://docs.cloud.deepset.ai/docs/api/main/health-health-get) |
| [List Datasets](actions/list-datasets.md) | `GET /api/v1/workspaces/:workspace_name/datasets` | [docs](https://docs.cloud.deepset.ai/docs/api/main/list-datasets-api-v-1-workspaces-workspace-name-datasets-get) |
| [List Files](actions/list-files.md) | `GET /api/v1/workspaces/:workspace_name/files` | [docs](https://docs.cloud.deepset.ai/docs/api/main/list-files-api-v-1-workspaces-workspace-name-files-get) |
| [List Indexes](actions/list-indexes.md) | `GET /api/v1/workspaces/:workspace_name/indexes` | [docs](https://docs.cloud.deepset.ai/docs/api/main/get-indexes-api-v-1-workspaces-workspace-name-indexes-get) |
| [List Pipelines](actions/list-pipelines.md) | `GET /api/v1/workspaces/:workspace_name/pipelines` | [docs](https://docs.cloud.deepset.ai/docs/api/main/list-pipelines-api-v-1-workspaces-workspace-name-pipelines-get) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/v1/workspaces` | [docs](https://docs.cloud.deepset.ai/docs/api/main/list-workspaces-api-v-1-workspaces-get) |
| [Query Documents](actions/query-documents.md) | `POST /api/v1/workspaces/:workspace_name/indexes/:index_name/documents-query` | [docs](https://docs.cloud.deepset.ai/docs/api/main/query-documents-api-v-1-workspaces-workspace-name-indexes-index-name-documents-query-post) |
| [Query Files](actions/query-files.md) | `POST /api/v1/workspaces/:workspace_name/files/_sql` | [docs](https://docs.cloud.deepset.ai/docs/api/main/query-files-api-v-1-workspaces-workspace-name-files-sql-post) |
| [Read Current User](actions/read-current-user.md) | `GET /api/v1/me` | [docs](https://docs.cloud.deepset.ai/docs/api/main/read-users-me-api-v-1-me-get) |
| [Search Pipeline](actions/search-pipeline.md) | `POST /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/search` | [docs](https://docs.cloud.deepset.ai/docs/api/main/search-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-search-post) |
