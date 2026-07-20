# <img src="https://images.mindcloud.co/apps/icons/openai_1773337005040.png" alt="Open AI logo" width="28" height="28"> Open AI: Universal API

Use OpenAI to generate text, images, audio, embeddings, videos, vector-store workflows, evals, and fine-tuning jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openAi/latest
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openai.com/
- **Vendor API docs:** https://developers.openai.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Transcribes audio in Open AI. |
| [Create Translation](actions/create-translation.md) | POST | Translates audio into English in Open AI. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT | Cancels a batch in Open AI. |
| [Create Batch](actions/create-batch.md) | POST | Creates a batch in Open AI. |
| [Retrieve Batch](actions/retrieve-batch.md) | GET | Retrieves a batch from Open AI. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a model response for the given chat conversation. |

### Compacted Response

| Action | Method | Description |
| --- | --- | --- |
| [Compact Response](actions/compact-response.md) | POST | Compacts a response in Open AI. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a conversation in Open AI. |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes a conversation from Open AI. |
| [Delete Conversation Item](actions/delete-conversation-item.md) | DELETE | Deletes an item from a conversation in Open AI. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Open AI. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates a conversation in Open AI. |

### Conversation Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Item](actions/create-conversation-item.md) | POST | Creates items in a conversation in Open AI. |
| [Get Conversation Item](actions/get-conversation-item.md) | GET | Retrieves an item from a conversation in Open AI. |
| [List Conversation Items](actions/list-conversation-items.md) | GET | Retrieves items from a conversation in Open AI. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embedding](actions/create-embedding.md) | POST | Creates text embeddings in Open AI. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Open AI. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Open AI. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Open AI. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Open AI. |

### File Content

| Action | Method | Description |
| --- | --- | --- |
| [Get File Content](actions/get-file-content.md) | GET | Retrieves file contents from Open AI. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Generates an image in Open AI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available models from Open AI. |
| [Retrieve Model](actions/retrieve-model.md) | GET | Retrieves a model from Open AI. |

### Moderation

| Action | Method | Description |
| --- | --- | --- |
| [Moderate Input](actions/moderate-input.md) | POST | Moderates text or image inputs in Open AI. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Response](actions/cancel-response.md) | PUT | Cancels a model response in Open AI. |
| [Create Response](actions/create-response.md) | POST | Creates a model response in Open AI. |
| [Delete Response](actions/delete-response.md) | DELETE | Deletes a model response from Open AI. |
| [Get Response](actions/get-response.md) | GET | Retrieves a model response from Open AI. |

### Response Input Item

| Action | Method | Description |
| --- | --- | --- |
| [List Response Input Items](actions/list-response-input-items.md) | GET | Retrieves input items from a response in Open AI. |

### Token Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Response Input Tokens](actions/count-response-input-tokens.md) | GET | Counts response input tokens in Open AI. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Vector Store](actions/delete-vector-store.md) | DELETE | Deletes a vector store from Open AI. |
| [Delete Vector Store File](actions/delete-vector-store-file.md) | DELETE | Deletes a vector store file from Open AI. |
| [Get Vector Store](actions/get-vector-store.md) | GET | Retrieves a vector store from Open AI. |
| [Get Vector Store File](actions/get-vector-store-file.md) | GET | Retrieves a vector store file from Open AI. |
| [Get Vector Store File Content](actions/get-vector-store-file-content.md) | GET | Retrieves vector store file contents from Open AI. |
| [List Vector Store Files](actions/list-vector-store-files.md) | GET | Retrieves vector store files from Open AI. |
| [List Vector Stores](actions/list-vector-stores.md) | GET | Retrieves vector stores from Open AI. |
| [Update Vector Store](actions/update-vector-store.md) | PUT | Updates a vector store in Open AI. |

### Vector Store

| Action | Method | Description |
| --- | --- | --- |
| [Create Vector Store](actions/create-vector-store.md) | POST | Creates a vector store in Open AI. |
| [Search Vector Store](actions/search-vector-store.md) | GET | Searches a vector store in Open AI. |

### Vector Store File

| Action | Method | Description |
| --- | --- | --- |
| [Add File To Vector Store](actions/add-file-to-vector-store.md) | POST | Adds a file to a vector store in Open AI. |

