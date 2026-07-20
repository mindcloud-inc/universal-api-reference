# <img src="https://images.mindcloud.co/apps/icons/images-2_1773688651760.jpeg" alt="Grok logo" width="28" height="28"> Grok: Universal API

Grok: Generate text, images, audio, video, and search documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grok/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://grok.com
- **Vendor API docs:** https://docs.x.ai/developers/rest-api-reference/inference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Key](actions/get-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key](actions/get-api-key.md) | GET | Retrieves the authenticated API key from Grok. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Processing on Batch](actions/cancel-processing-on-batch.md) | PUT | Cancels processing on an existing Grok batch. |
| [Create Batch](actions/create-batch.md) | POST | Creates a new batch in Grok. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a specific batch from Grok. |
| [List Batches](actions/list-batches.md) | GET | Retrieves a list of batches from Grok. |

### Batch Request

| Action | Method | Description |
| --- | --- | --- |
| [Add Batch Requests to Batch](actions/add-batch-requests-to-batch.md) | POST | Creates batch requests in a Grok batch. |
| [List Batch Requests](actions/list-batch-requests.md) | GET | Retrieves a list of requests in a Grok batch. |

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Processing Results of Batch](actions/get-processing-results-of-batch.md) | GET | Retrieves processing results for a Grok batch. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Grok. |
| [Get Deferred Chat Completions](actions/get-deferred-chat-completions.md) | GET | Retrieves deferred chat completion results from Grok. |

### Client Secret

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Secret](actions/create-client-secret.md) | POST | Creates a realtime client secret in Grok. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Search Content in Collection](actions/search-content-in-collection.md) | GET | Finds content in a Grok collection by search query. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a specific file from Grok. |
| [Get File Content](actions/get-file-content.md) | GET | Retrieves the content of a Grok file. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves metadata for a specific Grok file. |
| [List Files](actions/list-files.md) | GET | Retrieves a list of files from Grok. |
| [Update File](actions/update-file.md) | PUT | Updates a Grok file's metadata or content. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Grok. |

### File Chunk

| Action | Method | Description |
| --- | --- | --- |
| [Upload File in Chunks](actions/upload-file-in-chunks.md) | POST | Uploads file chunks to an existing Grok upload. |

### File Upload

| Action | Method | Description |
| --- | --- | --- |
| [Initialize File Upload](actions/initialize-file-upload.md) | POST | Creates a chunked file upload session in Grok. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Edit Image](actions/edit-image.md) | PUT | Updates an image in Grok with prompt-based edits. |
| [Generate Image](actions/generate-image.md) | POST | Creates images from prompts in Grok. |

### Image Generation Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Image Generation Model](actions/get-image-generation-model.md) | GET | Retrieves a specific image generation model from Grok. |
| [List Image Generation Models](actions/list-image-generation-models.md) | GET | Retrieves a list of image generation models from Grok. |

### Language Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Language Model](actions/get-language-model.md) | GET | Retrieves a specific language model from Grok. |
| [List Language Models](actions/list-language-models.md) | GET | Retrieves a list of language models from Grok. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET | Retrieves a specific model from Grok. |
| [List Models](actions/list-models.md) | GET | Retrieves a list of models from Grok. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create New Response](actions/create-new-response.md) | POST | Creates a new response in Grok. |
| [Delete Previous Response](actions/delete-previous-response.md) | DELETE | Deletes a previous response from Grok. |
| [Retrieve Previous Response](actions/retrieve-previous-response.md) | GET | Retrieves a previous response from Grok. |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Text to Speech](actions/text-to-speech.md) | POST | Creates speech audio from text in Grok. |

### Tokenization

| Action | Method | Description |
| --- | --- | --- |
| [Tokenize Text](actions/tokenize-text.md) | POST | Creates a tokenized representation of text in Grok. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Edit Video](actions/edit-video.md) | PUT | Updates a video in Grok with prompt-based edits. |
| [Generate Video](actions/generate-video.md) | POST | Creates a video generation request in Grok. |
| [Get Video Generation Results](actions/get-video-generation-results.md) | GET | Retrieves results for a video generation request from Grok. |

### Video Generation Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Generation Model](actions/get-video-generation-model.md) | GET | Retrieves a specific video generation model from Grok. |
| [List Video Generation Models](actions/list-video-generation-models.md) | GET | Retrieves a list of video generation models from Grok. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice](actions/get-voice.md) | GET | Retrieves a specific voice from Grok. |
| [List Voices](actions/list-voices.md) | GET | Retrieves a list of voices from Grok. |

