# Langfuse: Native API Reference

A consolidated summary of Langfuse's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://langfuse.com/docs/api-and-data-platform/features/public-api
- **OpenAPI specification:** https://cloud.langfuse.com/generated/api/openapi.yml
- **API base URL:** `https://cloud.langfuse.com/api/public`

## Authentication

### Basic Auth

Authenticate with the Langfuse public key as username and secret key as password.

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

[Official authentication documentation](https://langfuse.com/docs/api-and-data-platform/features/public-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.totalPages`. The current page number is read from `meta.page`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Annotation Queue](actions/create-annotation-queue.md) | `POST /annotation-queues` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/POST/api/public/annotation-queues) |
| [Create Annotation Queue Item](actions/create-annotation-queue-item.md) | `POST /annotation-queues/:queueId/items` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/POST/api/public/annotation-queues/{queueId}/items) |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://api.reference.langfuse.com/#tag/Comments/POST/api/public/comments) |
| [Create Dataset](actions/create-dataset.md) | `POST /v2/datasets` | [docs](https://api.reference.langfuse.com/#tag/Datasets/POST/api/public/v2/datasets) |
| [Create Dataset Item](actions/create-dataset-item.md) | `POST /dataset-items` | [docs](https://api.reference.langfuse.com/#tag/DatasetItems/POST/api/public/dataset-items) |
| [Create Dataset Run Item](actions/create-dataset-run-item.md) | `POST /dataset-run-items` | [docs](https://api.reference.langfuse.com/#tag/DatasetRunItems/POST/api/public/dataset-run-items) |
| [Create Prompt](actions/create-prompt.md) | `POST /v2/prompts` | [docs](https://api.reference.langfuse.com/#tag/Prompts/POST/api/public/v2/prompts) |
| [Create Score Config](actions/create-score-config.md) | `POST /score-configs` | [docs](https://api.reference.langfuse.com/#tag/ScoreConfigs/POST/api/public/score-configs) |
| [Delete Prompt](actions/delete-prompt.md) | `DELETE /v2/prompts/:promptName` | [docs](https://api.reference.langfuse.com/#tag/Prompts/DELETE/api/public/v2/prompts/{promptName}) |
| [Delete Trace](actions/delete-trace.md) | `DELETE /traces/:traceId` | [docs](https://api.reference.langfuse.com/#tag/Trace/DELETE/api/public/traces/{traceId}) |
| [Delete Traces](actions/delete-traces.md) | `DELETE /traces` | [docs](https://api.reference.langfuse.com/#tag/Trace/DELETE/api/public/traces) |
| [Get Annotation Queue](actions/get-annotation-queue.md) | `GET /annotation-queues/:queueId` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/GET/api/public/annotation-queues/{queueId}) |
| [Get Annotation Queue Item](actions/get-annotation-queue-item.md) | `GET /annotation-queues/:queueId/items/:itemId` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/GET/api/public/annotation-queues/{queueId}/items/{itemId}) |
| [Get Dataset](actions/get-dataset.md) | `GET /v2/datasets/:datasetName` | [docs](https://api.reference.langfuse.com/#tag/Datasets/GET/api/public/v2/datasets/{datasetName}) |
| [Get Dataset Item](actions/get-dataset-item.md) | `GET /dataset-items/:id` | [docs](https://api.reference.langfuse.com/#tag/DatasetItems/GET/api/public/dataset-items/{id}) |
| [Get Model](actions/get-model.md) | `GET /models/:id` | [docs](https://api.reference.langfuse.com/#tag/Models/GET/api/public/models/{id}) |
| [Get Project](actions/get-project.md) | `GET /projects` | [docs](https://api.reference.langfuse.com/#tag/Projects/GET/api/public/projects) |
| [Get Prompt](actions/get-prompt.md) | `GET /v2/prompts/:promptName` | [docs](https://api.reference.langfuse.com/#tag/Prompts/GET/api/public/v2/prompts/{promptName}) |
| [Get Score](actions/get-score.md) | `GET /v2/scores/:scoreId` | [docs](https://api.reference.langfuse.com/#tag/Scores/GET/api/public/v2/scores/{scoreId}) |
| [Get Score Config](actions/get-score-config.md) | `GET /score-configs/:configId` | [docs](https://api.reference.langfuse.com/#tag/ScoreConfigs/GET/api/public/score-configs/{configId}) |
| [Get Session](actions/get-session.md) | `GET /sessions/:sessionId` | [docs](https://api.reference.langfuse.com/#tag/Sessions/GET/api/public/sessions/{sessionId}) |
| [Get Trace](actions/get-trace.md) | `GET /traces/:traceId` | [docs](https://api.reference.langfuse.com/#tag/Trace/GET/api/public/traces/{traceId}) |
| [List Annotation Queue Items](actions/list-annotation-queue-items.md) | `GET /annotation-queues/:queueId/items` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/GET/api/public/annotation-queues/{queueId}/items) |
| [List Annotation Queues](actions/list-annotation-queues.md) | `GET /annotation-queues` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/GET/api/public/annotation-queues) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://api.reference.langfuse.com/#tag/Comments/GET/api/public/comments) |
| [List Dataset Items](actions/list-dataset-items.md) | `GET /dataset-items` | [docs](https://api.reference.langfuse.com/#tag/DatasetItems/GET/api/public/dataset-items) |
| [List Dataset Run Items](actions/list-dataset-run-items.md) | `GET /dataset-run-items` | [docs](https://api.reference.langfuse.com/#tag/DatasetRunItems/GET/api/public/dataset-run-items) |
| [List Dataset Runs](actions/list-dataset-runs.md) | `GET /datasets/:datasetName/runs` | [docs](https://api.reference.langfuse.com/#tag/Datasets/GET/api/public/datasets/{datasetName}/runs) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://api.reference.langfuse.com/#tag/Datasets/GET/api/public/v2/datasets) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://api.reference.langfuse.com/#tag/Models/GET/api/public/models) |
| [List Observations](actions/list-observations.md) | `GET /v2/observations` | [docs](https://api.reference.langfuse.com/#tag/Observations/GET/api/public/v2/observations) |
| [List Prompts](actions/list-prompts.md) | `GET /v2/prompts` | [docs](https://api.reference.langfuse.com/#tag/Prompts/GET/api/public/v2/prompts) |
| [List Score Configs](actions/list-score-configs.md) | `GET /score-configs` | [docs](https://api.reference.langfuse.com/#tag/ScoreConfigs/GET/api/public/score-configs) |
| [List Scores](actions/list-scores.md) | `GET /v2/scores` | [docs](https://api.reference.langfuse.com/#tag/Scores/GET/api/public/v2/scores) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://api.reference.langfuse.com/#tag/Sessions/GET/api/public/sessions) |
| [List Traces](actions/list-traces.md) | `GET /traces` | [docs](https://api.reference.langfuse.com/#tag/Trace/GET/api/public/traces) |
| [Query Metrics](actions/query-metrics.md) | `GET /v2/metrics` | [docs](https://api.reference.langfuse.com/#tag/Metrics/GET/api/public/v2/metrics) |
| [Update Annotation Queue Item](actions/update-annotation-queue-item.md) | `PATCH /annotation-queues/:queueId/items/:itemId` | [docs](https://api.reference.langfuse.com/#tag/AnnotationQueues/PATCH/api/public/annotation-queues/{queueId}/items/{itemId}) |
| [Update Prompt Version](actions/update-prompt-version.md) | `PATCH /v2/prompts/:name/versions/:version` | [docs](https://api.reference.langfuse.com/#tag/PromptVersion/PATCH/api/public/v2/prompts/{name}/versions/{version}) |
| [Update Score Config](actions/update-score-config.md) | `PATCH /score-configs/:configId` | [docs](https://api.reference.langfuse.com/#tag/ScoreConfigs/PATCH/api/public/score-configs/{configId}) |
