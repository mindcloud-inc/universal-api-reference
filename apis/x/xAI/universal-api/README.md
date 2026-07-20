# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-x-ai-48x48_1778074376704.png" alt="xAI logo" width="28" height="28"> xAI: Universal API

Use xAI Grok models and related inference APIs for responses, chat completions, model discovery, image generation, video generation, batches, files, and voice utilities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xAI/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://x.ai
- **Vendor API docs:** https://docs.x.ai/developers/rest-api-reference/inference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Text To Speech](actions/create-text-to-speech.md) | POST | Creates text-to-speech audio in the xAI API. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT | Cancels a batch in the xAI API. |
| [Create Batch](actions/create-batch.md) | POST | Creates a batch in the xAI API. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch from the xAI API. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches from the xAI API. |

### Batch Request

| Action | Method | Description |
| --- | --- | --- |
| [Add Batch Requests](actions/add-batch-requests.md) | POST | Adds batch requests in the xAI API. |
| [List Batch Requests](actions/list-batch-requests.md) | GET | Retrieves batch requests from the xAI API. |

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [List Batch Results](actions/list-batch-results.md) | GET | Retrieves batch results from the xAI API. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in the xAI API. |
| [Get Deferred Chat Completion](actions/get-deferred-chat-completion.md) | GET | Retrieves deferred chat completions from the xAI API. |

### Document Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in the xAI API. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from the xAI API. |
| [List Files](actions/list-files.md) | GET | Retrieves files from the xAI API. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from the xAI API. |

### File Content

| Action | Method | Description |
| --- | --- | --- |
| [Download File Content](actions/download-file-content.md) | GET | Downloads file content from the xAI API. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Edit Image](actions/edit-image.md) | PUT | Edits an image in the xAI API. |
| [Generate Image](actions/generate-image.md) | POST | Creates an image in the xAI API. |

### Image Generation Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Image Generation Model](actions/get-image-generation-model.md) | GET | Retrieves an image generation model from the xAI API. |
| [List Image Generation Models](actions/list-image-generation-models.md) | GET | Retrieves image generation models from the xAI API. |

### Language Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Language Model](actions/get-language-model.md) | GET | Retrieves a language model from the xAI API. |
| [List Language Models](actions/list-language-models.md) | GET | Retrieves language models from the xAI API. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Anthropic Message](actions/create-anthropic-message.md) | POST | Creates an Anthropic-style message in the xAI API. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from the xAI API. |
| [List Models](actions/list-models.md) | GET | Retrieves models from the xAI API. |

### Realtime Client Secret

| Action | Method | Description |
| --- | --- | --- |
| [Create Realtime Client Secret](actions/create-realtime-client-secret.md) | POST | Creates a realtime client secret in the xAI API. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a response in the xAI API. |
| [Delete Response](actions/delete-response.md) | DELETE | Deletes a response from the xAI API. |
| [Retrieve Response](actions/retrieve-response.md) | GET | Retrieves a response from the xAI API. |

### Text Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Legacy Text Completion](actions/create-legacy-text-completion.md) | POST | Creates a legacy text completion in the xAI API. |

### Tts Voice

| Action | Method | Description |
| --- | --- | --- |
| [Get TTS Voice](actions/get-tts-voice.md) | GET | Retrieves a text-to-speech voice from the xAI API. |
| [List TTS Voices](actions/list-tts-voices.md) | GET | Retrieves text-to-speech voices from the xAI API. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Edit Video](actions/edit-video.md) | PUT | Edits a video in the xAI API. |
| [Extend Video](actions/extend-video.md) | PUT | Extends a video in the xAI API. |
| [Generate Video](actions/generate-video.md) | POST | Creates a video in the xAI API. |
| [Get Video Result](actions/get-video-result.md) | GET | Retrieves a video result from the xAI API. |

### Video Generation Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Generation Model](actions/get-video-generation-model.md) | GET | Retrieves a video generation model from the xAI API. |
| [List Video Generation Models](actions/list-video-generation-models.md) | GET | Retrieves video generation models from the xAI API. |

