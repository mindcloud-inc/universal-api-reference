# Dremio: Native API Reference

A consolidated summary of Dremio's API configuration and 63 documented operations, with links to official documentation.

- **Official docs:** https://docs.dremio.com/dremio-cloud/api/
- **API base URL:** `https://api.dremio.cloud/v0`

## Authentication

### Personal Access Token

Authenticate Dremio Cloud API requests with a Personal Access Token sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dremio.com/dremio-cloud/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Dremio project UUID. |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (63 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Delete Scripts](actions/batch-delete-scripts.md) | `POST /projects/:project_id/scripts:batchDelete` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Cancel Job](actions/cancel-job.md) | `POST /projects/:project_id/job/:id/cancel` | [docs](https://docs.dremio.com/dremio-cloud/api/job/) |
| [Clear Source Permission Cache](actions/clear-source-permission-cache.md) | `DELETE /projects/:project_id/source/:source_name/permission-cache` | [docs](https://docs.dremio.com/dremio-cloud/api/source/) |
| [Create Engine](actions/create-engine.md) | `POST /projects/:project_id/engines` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [Create External Token Provider](actions/create-external-token-provider.md) | `POST /external-token-providers` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [Create Identity Provider](actions/create-identity-provider.md) | `POST /identity-providers` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [Create Maintenance Task](actions/create-maintenance-task.md) | `POST /projects/:project_id/maintenance/tasks` | [docs](https://docs.dremio.com/dremio-cloud/api/data-maintenance/) |
| [Create Personal Access Token](actions/create-personal-access-token.md) | `POST /user/:user_id/token` | [docs](https://docs.dremio.com/dremio-cloud/api/) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://docs.dremio.com/dremio-cloud/api/projects/) |
| [Create Reflection](actions/create-reflection.md) | `POST /projects/:project_id/reflection` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [Create Script](actions/create-script.md) | `POST /projects/:project_id/scripts` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Delete Engine](actions/delete-engine.md) | `DELETE /projects/:project_id/engines/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [Delete External Token Provider](actions/delete-external-token-provider.md) | `DELETE /external-token-providers/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [Delete Identity Provider](actions/delete-identity-provider.md) | `DELETE /identity-providers/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [Delete Maintenance Task](actions/delete-maintenance-task.md) | `DELETE /projects/:project_id/maintenance/tasks/:taskId` | [docs](https://docs.dremio.com/dremio-cloud/api/data-maintenance/) |
| [Delete Personal Access Token](actions/delete-personal-access-token.md) | `DELETE /user/:user_id/token` | [docs](https://docs.dremio.com/dremio-cloud/api/) |
| [Delete Personal Access Token By ID](actions/delete-personal-access-token-by-id.md) | `DELETE /user/:user_id/token/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/projects/) |
| [Delete Reflection](actions/delete-reflection.md) | `DELETE /projects/:project_id/reflection/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [Delete Script](actions/delete-script.md) | `DELETE /projects/:project_id/scripts/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Disable Engine](actions/disable-engine.md) | `PUT /projects/:project_id/engines/:id/disable` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [Disable External Token Provider](actions/disable-external-token-provider.md) | `PUT /external-token-providers/:id/disable` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [Disable Identity Provider](actions/disable-identity-provider.md) | `PUT /identity-providers/:id/disable` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [Enable Engine](actions/enable-engine.md) | `PUT /projects/:project_id/engines/:id/enable` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [Enable External Token Provider](actions/enable-external-token-provider.md) | `PUT /external-token-providers/:id/enable` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [Enable Identity Provider](actions/enable-identity-provider.md) | `PUT /identity-providers/:id/enable` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [Get Catalog Grants](actions/get-catalog-grants.md) | `GET /projects/:project_id/catalog/:id/grants` | [docs](https://docs.dremio.com/dremio-cloud/api/catalog/grants/) |
| [Get Dataset](actions/get-dataset.md) | `GET /projects/:project_id/catalog/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/catalog/dataset/) |
| [Get Engine](actions/get-engine.md) | `GET /projects/:project_id/engines/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [Get External Token Provider](actions/get-external-token-provider.md) | `GET /external-token-providers/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [Get Folder](actions/get-folder.md) | `GET /projects/:project_id/catalog/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/catalog/folder/) |
| [Get Identity Provider](actions/get-identity-provider.md) | `GET /identity-providers/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [Get Job](actions/get-job.md) | `GET /projects/:project_id/job/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/job/) |
| [Get Job Results](actions/get-job-results.md) | `GET /projects/:project_id/job/:id/results` | [docs](https://docs.dremio.com/dremio-cloud/api/job/) |
| [Get Maintenance Task](actions/get-maintenance-task.md) | `GET /projects/:project_id/maintenance/tasks/:taskId` | [docs](https://docs.dremio.com/dremio-cloud/api/data-maintenance/) |
| [Get Personal Access Tokens](actions/get-personal-access-tokens.md) | `GET /user/:user_id/token` | [docs](https://docs.dremio.com/dremio-cloud/api/) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/projects/) |
| [Get Reflection Summary](actions/get-reflection-summary.md) | `GET /projects/:project_id/reflection/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [Get Script](actions/get-script.md) | `GET /projects/:project_id/scripts/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Get Script Grants](actions/get-script-grants.md) | `GET /projects/:project_id/scripts/:id/grants` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Get Source](actions/get-source.md) | `GET /projects/:project_id/catalog/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/catalog/source/) |
| [List Catalog](actions/list-catalog.md) | `GET /projects/:project_id/catalog` | [docs](https://docs.dremio.com/dremio-cloud/api/catalog/) |
| [List Dataset Reflections](actions/list-dataset-reflections.md) | `GET /projects/:project_id/dataset/:datasetId/reflection` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [List Engine Rules](actions/list-engine-rules.md) | `GET /projects/:project_id/rules` | [docs](https://docs.dremio.com/dremio-cloud/api/rules/) |
| [List Engines](actions/list-engines.md) | `GET /projects/:project_id/engines` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [List External Token Providers](actions/list-external-token-providers.md) | `GET /external-token-providers` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [List Identity Providers](actions/list-identity-providers.md) | `GET /identity-providers` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [List Maintenance Tasks](actions/list-maintenance-tasks.md) | `GET /projects/:project_id/maintenance/tasks` | [docs](https://docs.dremio.com/dremio-cloud/api/data-maintenance/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.dremio.com/dremio-cloud/api/projects/) |
| [List Reflections](actions/list-reflections.md) | `GET /projects/:project_id/reflection` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [List Scripts](actions/list-scripts.md) | `GET /projects/:project_id/scripts` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Refresh Reflection](actions/refresh-reflection.md) | `POST /projects/:project_id/reflection/:id/refresh` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [Search](actions/search.md) | `POST /projects/:project_id/search` | [docs](https://docs.dremio.com/dremio-cloud/api/search/) |
| [Submit SQL Query](actions/submit-sql-query.md) | `POST /projects/:project_id/sql` | [docs](https://docs.dremio.com/dremio-cloud/api/sql/) |
| [Update Catalog Grants](actions/update-catalog-grants.md) | `PUT /projects/:project_id/catalog/:id/grants` | [docs](https://docs.dremio.com/dremio-cloud/api/catalog/grants/) |
| [Update Engine](actions/update-engine.md) | `PUT /projects/:project_id/engines/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/engines/) |
| [Update External Token Provider](actions/update-external-token-provider.md) | `PUT /external-token-providers/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/external-token-providers/) |
| [Update Identity Provider](actions/update-identity-provider.md) | `PUT /identity-providers/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/identity-providers/) |
| [Update Maintenance Task](actions/update-maintenance-task.md) | `PUT /projects/:project_id/maintenance/tasks/:taskId` | [docs](https://docs.dremio.com/dremio-cloud/api/data-maintenance/) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/projects/) |
| [Update Reflection](actions/update-reflection.md) | `PUT /projects/:project_id/reflection/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/reflection/) |
| [Update Script](actions/update-script.md) | `PATCH /projects/:project_id/scripts/:id` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
| [Update Script Grants](actions/update-script-grants.md) | `PUT /projects/:project_id/scripts/:id/grants` | [docs](https://docs.dremio.com/dremio-cloud/api/scripts/) |
