# <img src="https://images.mindcloud.co/apps/icons/mistral-ai_1773918760750.png" alt="Mistral AI logo" width="28" height="28"> Mistral AI: Universal API

Generate, classify, transcribe, and extract content with Mistral AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mistralAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mistral.ai
- **Vendor API docs:** https://docs.mistral.ai/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Agent Completion

| Action | Method | Description |
| --- | --- | --- |
| [Agents Completion](actions/agents-completion.md) | POST | Creates an agent completion in Mistral AI. |

### Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch Job](actions/cancel-batch-job.md) | PUT | Cancels an existing batch job in Mistral AI. |
| [Create Batch Job](actions/create-batch-job.md) | POST | Creates a new batch job in Mistral AI. |
| [Get Batch Job](actions/get-batch-job.md) | GET | Retrieves batch job details from Mistral AI. |
| [List Batch Jobs](actions/list-batch-jobs.md) | GET | Retrieves batch jobs from Mistral AI. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Chat Completion](actions/chat-completion.md) | POST | Creates a chat completion in Mistral AI. |

### Chat Moderation

| Action | Method | Description |
| --- | --- | --- |
| [Chat Moderations](actions/chat-moderations.md) | POST | Creates chat moderation results in Mistral AI. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Embeddings](actions/embeddings.md) | POST | Creates text embeddings in Mistral AI. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Mistral AI. |
| [Download File](actions/download-file.md) | GET | Retrieves file content from Mistral AI. |
| [Get Signed URL](actions/get-signed-url.md) | GET | Retrieves a signed file URL from Mistral AI. |
| [List Files](actions/list-files.md) | GET | Retrieves available files from Mistral AI. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves file details from Mistral AI. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Mistral AI. |

### Fim Completion

| Action | Method | Description |
| --- | --- | --- |
| [FIM Completion](actions/fim-completion.md) | POST | Creates a fill-in-the-middle completion in Mistral AI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Delete Fine Tuned Model](actions/delete-fine-tuned-model.md) | DELETE | Deletes an existing fine-tuned model from Mistral AI. |
| [List Models](actions/list-models.md) | GET | Retrieves available models from Mistral AI. |
| [Retrieve Model](actions/retrieve-model.md) | GET | Retrieves model details from Mistral AI. |
| [Update Fine Tuned Model](actions/update-fine-tuned-model.md) | PUT | Updates an existing fine-tuned model in Mistral AI. |

### Moderation

| Action | Method | Description |
| --- | --- | --- |
| [Moderations](actions/moderations.md) | POST | Creates text moderation results in Mistral AI. |

### Ocr Result

| Action | Method | Description |
| --- | --- | --- |
| [OCR](actions/ocr.md) | POST | Creates OCR results for a document in Mistral AI. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Creates an audio transcription in Mistral AI. |

