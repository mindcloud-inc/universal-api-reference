# Gemini: Native API Reference

A consolidated summary of Gemini's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://ai.google.dev/api
- **OpenAPI specification:** https://generativelanguage.googleapis.com/$discovery/OPENAPI3_0?version=v1beta
- **API base URL:** `https://generativelanguage.googleapis.com`

## Authentication

### Gemini API Key

Primary Gemini authentication using API key in query parameter `key`.

### Credentials

- **API Key:** `apiKey` · required · Required Gemini API key sent as query parameter `key`.

[Official authentication documentation](https://ai.google.dev/gemini-api/docs/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Async Batch Embed Content](actions/async-batch-embed-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/batch-api#method:-models.asyncbatchembedcontent) |
| [Batch Embed Contents](actions/batch-embed-contents.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/embeddings#method:-models.batchembedcontents) |
| [Batch Generate Content](actions/batch-generate-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/batch-api#method:-models.batchgeneratecontent) |
| [Cancel Batch](actions/cancel-batch.md) | `POST v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api#method:-batches.cancel) |
| [Count Tokens](actions/count-tokens.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/tokens#method:-models.counttokens) |
| [Create Cached Content](actions/create-cached-content.md) | `POST v1beta/cachedContents` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.create) |
| [Delete Batch](actions/delete-batch.md) | `DELETE v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api#method:-batches.delete) |
| [Delete Cached Content](actions/delete-cached-content.md) | `DELETE v1beta/cachedContents/:cachedContentId` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.delete) |
| [Delete File](actions/delete-file.md) | `DELETE v1beta/files/:fileId` | [docs](https://ai.google.dev/api/files#method:-files.delete) |
| [Embed Content](actions/embed-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/embeddings#method:-models.embedcontent) |
| [Generate Content](actions/generate-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/generate-content#method:-models.generatecontent) |
| [Generate Content (Tuned Model)](actions/generate-content-tuned-model.md) | `POST v1beta/tunedModels/:model` | [docs](https://ai.google.dev/api/tuning#method:-tunedmodels.generatecontent) |
| [Get Batch](actions/get-batch.md) | `GET v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api#method:-batches.get) |
| [Get Cached Content](actions/get-cached-content.md) | `GET v1beta/cachedContents/:cachedContentId` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.get) |
| [Get File](actions/get-file.md) | `GET v1beta/files/:fileId` | [docs](https://ai.google.dev/api/files#method:-files.get) |
| [Get Model](actions/get-model.md) | `GET v1beta/models/:model` | [docs](https://ai.google.dev/api/models#v1beta.models.get) |
| [List Batches](actions/list-batches.md) | `GET v1beta/:name` | [docs](https://ai.google.dev/api/batch-api#method:-batches.list) |
| [List Cached Contents](actions/list-cached-contents.md) | `GET v1beta/cachedContents` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.list) |
| [List Files](actions/list-files.md) | `GET v1beta/files` | [docs](https://ai.google.dev/api/files#method:-files.list) |
| [List Models](actions/list-models.md) | `GET v1beta/models` | [docs](https://ai.google.dev/api/models#v1beta.models.list) |
| [List Tuned Models](actions/list-tuned-models.md) | `GET v1beta/tunedModels` | [docs](https://ai.google.dev/api/tuning#method:-tunedmodels.list) |
| [Predict Long Running](actions/predict-long-running.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/models#v1beta.models.predictLongRunning) |
| [Register File](actions/register-file.md) | `POST v1beta/files:register` | [docs](https://ai.google.dev/api/files#method:-files.register) |
| [Stream Generate Content](actions/stream-generate-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/generate-content#method:-models.streamgeneratecontent) |
| [Update Cached Content](actions/update-cached-content.md) | `PATCH v1beta/cachedContents/:cachedContentId` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.patch) |
| [Update Embed Content Batch](actions/update-embed-content-batch.md) | `PATCH v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api#method:-batches.updateembedcontentbatch) |
| [Update Generate Content Batch](actions/update-generate-content-batch.md) | `PATCH v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api#method:-batches.updategeneratecontentbatch) |
| [Upload File Media](actions/upload-file-media.md) | `POST v1beta/files` | [docs](https://ai.google.dev/api/files#method:-media.upload) |
