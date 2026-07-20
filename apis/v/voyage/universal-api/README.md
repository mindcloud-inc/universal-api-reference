# <img src="https://images.mindcloud.co/apps/icons/voyage-ai_1776804371129.png" alt="Voyage logo" width="28" height="28"> Voyage: Universal API

Generate embeddings, rerank results, and manage Voyage batch jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voyage/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.voyageai.com/
- **Vendor API docs:** https://docs.voyageai.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | PUT | Cancels an in-progress batch in Voyage. |
| [Create Batch](actions/create-batch.md) | POST | Creates and executes a batch in Voyage. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches for your Voyage organization. |
| [Retrieve Batch](actions/retrieve-batch.md) | GET | Retrieves a batch from Voyage. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Generate Contextualized Embeddings](actions/generate-contextualized-embeddings.md) | POST | Generates contextualized chunk embeddings in Voyage. |
| [Generate Multimodal Embeddings](actions/generate-multimodal-embeddings.md) | POST | Generates multimodal embeddings in Voyage. |
| [Generate Text Embeddings](actions/generate-text-embeddings.md) | POST | Generates text vector embeddings in Voyage. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves files from Voyage. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from Voyage. |
| [Retrieve File Content](actions/retrieve-file-content.md) | GET | Retrieves the contents of a file from Voyage. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file for Voyage batch processing. |

### Rerank Result

| Action | Method | Description |
| --- | --- | --- |
| [Rerank Documents](actions/rerank-documents.md) | POST | Reranks documents in Voyage for a query. |

