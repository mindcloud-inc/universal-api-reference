# <img src="https://images.mindcloud.co/apps/icons/gemini_1772650690852.png" alt="Gemini logo" width="28" height="28"> Gemini: Universal API

Generate text, images, audio, video, and agent workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gemini/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ai.google.dev/
- **Vendor API docs:** https://ai.google.dev/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT | Cancels a batch operation in Gemini. |
| [Delete Batch](actions/delete-batch.md) | DELETE | Deletes a batch operation from Gemini. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch operation from Gemini. |
| [List Batches](actions/list-batches.md) | GET | Retrieves a list of batches from Gemini. |
| [Update Embed Content Batch](actions/update-embed-content-batch.md) | PUT | Updates an embed content batch in Gemini. |
| [Update Generate Content Batch](actions/update-generate-content-batch.md) | PUT | Updates a generate content batch in Gemini. |

### Cached Content

| Action | Method | Description |
| --- | --- | --- |
| [Create Cached Content](actions/create-cached-content.md) | POST | Creates a cached content resource in Gemini. |
| [Delete Cached Content](actions/delete-cached-content.md) | DELETE | Deletes a cached content resource from Gemini. |
| [Get Cached Content](actions/get-cached-content.md) | GET | Retrieves a cached content resource from Gemini. |
| [List Cached Contents](actions/list-cached-contents.md) | GET | Retrieves a list of cached content resources from Gemini. |
| [Update Cached Content](actions/update-cached-content.md) | PUT | Updates a cached content resource in Gemini. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Gemini. |
| [Get File](actions/get-file.md) | GET | Retrieves the metadata for a file from Gemini. |
| [List Files](actions/list-files.md) | GET | Retrieves a list of files from Gemini. |
| [Register File](actions/register-file.md) | POST | Registers a Cloud Storage file with Gemini. |
| [Upload File Media](actions/upload-file-media.md) | POST | Uploads a file to Gemini. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Async Batch Embed Content](actions/async-batch-embed-content.md) | POST | Enqueues a batch embed content job in Gemini. |
| [Batch Embed Contents](actions/batch-embed-contents.md) | POST | Generates multiple content embeddings with Gemini. |
| [Batch Generate Content](actions/batch-generate-content.md) | POST | Enqueues a batch generate content job in Gemini. |
| [Count Tokens](actions/count-tokens.md) | GET | Counts tokens for content in Gemini. |
| [Embed Content](actions/embed-content.md) | POST | Generates content embeddings with Gemini. |
| [Generate Content](actions/generate-content.md) | POST | Generates content with a Gemini model. |
| [Get Model](actions/get-model.md) | GET | Retrieves metadata for a model from Gemini. |
| [List Models](actions/list-models.md) | GET | Retrieves a list of models from Gemini. |
| [Predict Long Running](actions/predict-long-running.md) | POST | Starts a long-running prediction in Gemini. |
| [Stream Generate Content](actions/stream-generate-content.md) | POST | Generates streamed content with a Gemini model. |

### Tuned Model

| Action | Method | Description |
| --- | --- | --- |
| [List Tuned Models](actions/list-tuned-models.md) | GET | Retrieves created tuned models from Gemini. |

### Tuned Model Response

| Action | Method | Description |
| --- | --- | --- |
| [Generate Content (Tuned Model)](actions/generate-content-tuned-model.md) | POST | Generates content with a tuned model in Gemini. |

