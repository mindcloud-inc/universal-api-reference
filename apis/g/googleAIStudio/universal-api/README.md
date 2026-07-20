# <img src="https://images.mindcloud.co/apps/icons/google-aistudio_1774363352859.png" alt="Google AI Studio logo" width="28" height="28"> Google AI Studio: Universal API

Generate multimodal content, embeddings, files, and batch jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleAIStudio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aistudio.google.com/
- **Vendor API docs:** https://ai.google.dev/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT | Cancels a batch operation in Google AI Studio. |
| [Delete Batch](actions/delete-batch.md) | DELETE | Deletes a batch operation from Google AI Studio. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch operation from Google AI Studio. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batch operations from Google AI Studio. |

### Cached Content

| Action | Method | Description |
| --- | --- | --- |
| [Create Cached Content](actions/create-cached-content.md) | POST | Creates a cached content entry in Google AI Studio. |
| [Delete Cached Content](actions/delete-cached-content.md) | DELETE | Deletes a cached content entry from Google AI Studio. |
| [Get Cached Content](actions/get-cached-content.md) | GET | Retrieves a cached content entry from Google AI Studio. |
| [List Cached Contents](actions/list-cached-contents.md) | GET | Retrieves cached content entries from Google AI Studio. |
| [Update Cached Content](actions/update-cached-content.md) | PUT | Updates cached content expiration in Google AI Studio. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Google AI Studio. |
| [Get File](actions/get-file.md) | GET | Retrieves file metadata from Google AI Studio. |
| [List Files](actions/list-files.md) | GET | Retrieves file metadata for your Google AI Studio project. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Count Tokens](actions/count-tokens.md) | GET | Counts prompt tokens for a Gemini model in Google AI Studio. |
| [Embed Content](actions/embed-content.md) | POST | Generates text embeddings with a Gemini model in Google AI Studio. |
| [Generate Content](actions/generate-content.md) | POST | Generates content with a Gemini model in Google AI Studio. |
| [Get Model](actions/get-model.md) | GET | Retrieves a Gemini model from Google AI Studio. |
| [List Models](actions/list-models.md) | GET | Retrieves available Gemini models from Google AI Studio. |
| [Stream Generate Content](actions/stream-generate-content.md) | POST | Generates streamed content with a Gemini model in Google AI Studio. |

