# Cerebras AI: Native API Reference

A consolidated summary of Cerebras AI's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://inference-docs.cerebras.ai/api-reference/versions
- **API base URL:** `https://api.cerebras.ai`

## Authentication

### API Key

Authenticate Cerebras inference API requests with a Cerebras API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://inference-docs.cerebras.ai/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | `DELETE /v1/batches/:batchId` | [docs](https://inference-docs.cerebras.ai/api-reference/batch/cancel-batch) |
| [Create Batch](actions/create-batch.md) | `POST /v1/batches` | [docs](https://inference-docs.cerebras.ai/api-reference/batch/create-batch) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://inference-docs.cerebras.ai/api-reference/chat-completions) |
| [Create Completion](actions/create-completion.md) | `POST /v1/completions` | [docs](https://inference-docs.cerebras.ai/api-reference/completions) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/files/:fileId` | [docs](https://inference-docs.cerebras.ai/api-reference/file/delete-file) |
| [Delete Model Version](actions/delete-model-version.md) | `DELETE /management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/delete-model-version) |
| [Deploy Model To Endpoint](actions/deploy-model-to-endpoint.md) | `POST /management/v1/endpoints/:endpointId:deployModel` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/deploy-model-to-endpoint) |
| [List Batches](actions/list-batches.md) | `GET /v1/batches` | [docs](https://inference-docs.cerebras.ai/api-reference/batch/list-batch) |
| [List Endpoints](actions/list-endpoints.md) | `GET /management/v1/orgs/:orgName/endpoints` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/list-endpoints) |
| [List Files](actions/list-files.md) | `GET /v1/files/` | [docs](https://inference-docs.cerebras.ai/api-reference/file/list-files) |
| [List Model Architectures](actions/list-model-architectures.md) | `GET /management/v1/orgs/:orgName/models` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/list-model-architectures) |
| [List Model Versions](actions/list-model-versions.md) | `GET /management/v1/orgs/:orgName/models/:modelArchId/versions` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/list-model-versions) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://inference-docs.cerebras.ai/api-reference/models/list-models) |
| [List Public Models](actions/list-public-models.md) | `GET /public/v1/models` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [List Public Models (Generic Format)](actions/list-public-models-by-format.md) | `GET /public/v1/models` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [List Public Models (HuggingFace)](actions/list-public-models-hugging-face.md) | `GET /public/v1/models` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [List Public Models (OpenRouter)](actions/list-public-models-open-router.md) | `GET /public/v1/models` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [Retrieve Batch](actions/retrieve-batch.md) | `GET /v1/batches/:batchId` | [docs](https://inference-docs.cerebras.ai/api-reference/batch/retrieve-batch) |
| [Retrieve Batch Results](actions/retrieve-batch-results.md) | `GET /v1/batches/:batchId/results` | [docs](https://inference-docs.cerebras.ai/api-reference/batch/retrieve-batch-results) |
| [Retrieve Endpoint Status](actions/retrieve-endpoint-status.md) | `GET /management/v1/endpoints/:endpointId` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/retrieve-endpoint-status) |
| [Retrieve File](actions/retrieve-file.md) | `GET /v1/files/:fileId` | [docs](https://inference-docs.cerebras.ai/api-reference/file/retrieve-file) |
| [Retrieve File Content](actions/retrieve-file-content.md) | `GET /v1/files/:fileId/content` | [docs](https://inference-docs.cerebras.ai/api-reference/file/retrieve-file-content) |
| [Retrieve Metrics](actions/retrieve-metrics.md) | `GET https://cloud.cerebras.ai/api/v1/metrics/organizations/:organizationId` | [docs](https://inference-docs.cerebras.ai/api-reference/metrics/retrieve-metrics) |
| [Retrieve Model](actions/retrieve-model.md) | `GET /v1/models/:modelId` | [docs](https://inference-docs.cerebras.ai/api-reference/models/retrieve-model) |
| [Retrieve Model Version Status](actions/retrieve-model-version-status.md) | `GET /management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/retrieve-model-version-status) |
| [Retrieve Public Model](actions/retrieve-public-model.md) | `GET /public/v1/models/:modelId` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [Retrieve Public Model (Generic Format)](actions/retrieve-public-model-by-format.md) | `GET /public/v1/models/:modelId` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [Retrieve Public Model (HuggingFace)](actions/retrieve-public-model-hugging-face.md) | `GET /public/v1/models/:modelId` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [Retrieve Public Model (OpenRouter)](actions/retrieve-public-model-open-router.md) | `GET /public/v1/models/:modelId` | [docs](https://inference-docs.cerebras.ai/api-reference/models/public-models) |
| [Update Model Version Aliases](actions/update-model-version-aliases.md) | `PATCH /management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/update-model-version-aliases) |
| [Upload File](actions/upload-file.md) | `POST /v1/files` | [docs](https://inference-docs.cerebras.ai/api-reference/file/upload-file) |
| [Upload Model Version](actions/upload-model-version.md) | `POST /management/v1/orgs/:orgName/models:upload` | [docs](https://inference-docs.cerebras.ai/api-reference/customer_management_api/upload-model-version) |
