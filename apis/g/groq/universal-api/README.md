# <img src="https://images.mindcloud.co/apps/icons/groq_1773777967868.png" alt="Groq logo" width="28" height="28"> Groq: Universal API

Groq provides high-speed AI inference APIs for chat completions, responses, embeddings, reranking, audio, files, batches, and fine-tuning workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/groq/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://groq.com
- **Vendor API docs:** https://console.groq.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groq/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT | Cancels a batch in Groq. |
| [Create Batch](actions/create-batch.md) | POST | Creates a batch in Groq. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches from Groq. |
| [Retrieve Batch](actions/retrieve-batch.md) | GET | Retrieves a batch from Groq. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Groq. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embedding](actions/create-embedding.md) | POST | Creates an embedding in Groq. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Groq. |
| [Download File](actions/download-file.md) | GET | Downloads a file from Groq. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Groq. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from Groq. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Groq. |

### Fine Tuning

| Action | Method | Description |
| --- | --- | --- |
| [Create Fine Tuning](actions/create-fine-tuning.md) | POST | Creates a fine-tuning job in Groq. |
| [Delete Fine Tuning](actions/delete-fine-tuning.md) | DELETE | Deletes a fine-tuning job from Groq. |
| [Get Fine Tuning](actions/get-fine-tuning.md) | GET | Retrieves a fine-tuning job from Groq. |
| [List Fine Tunings](actions/list-fine-tunings.md) | GET | Retrieves fine-tuning jobs from Groq. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Delete Model](actions/delete-model.md) | DELETE | Deletes a model from Groq. |
| [List Models](actions/list-models.md) | GET | Retrieves models from Groq. |
| [Retrieve Model](actions/retrieve-model.md) | GET | Retrieves a model from Groq. |

### Reranking

| Action | Method | Description |
| --- | --- | --- |
| [Create Reranking](actions/create-reranking.md) | POST | Creates a reranking result in Groq. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a response in Groq. |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech](actions/create-speech.md) | POST | Creates speech from text in Groq. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Creates a transcription from audio in Groq. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation](actions/create-translation.md) | POST | Creates an audio translation in Groq. |

