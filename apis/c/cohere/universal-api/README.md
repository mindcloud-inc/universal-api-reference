# <img src="https://images.mindcloud.co/apps/icons/cohere-icon_1775483772218.png" alt="Cohere logo" width="28" height="28"> Cohere: Universal API

Access Cohere's chat, embeddings, reranking, tokenization, dataset, connector, fine-tuning, and batch APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cohere/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cohere.com/
- **Vendor API docs:** https://docs.cohere.com/reference/about

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Dataset](actions/delete-dataset.md) | DELETE | Deletes a dataset from Cohere. |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from Cohere. |
| [Get Dataset Usage](actions/get-dataset-usage.md) | GET | Retrieves dataset usage details from Cohere. |
| [List Datasets](actions/list-datasets.md) | GET | Lists available training datasets in Cohere. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Detokenize](actions/detokenize.md) | GET | Converts Cohere token IDs back into text. |
| [Embed](actions/embed.md) | GET | Generates embeddings for text or images in Cohere. |
| [Rerank](actions/rerank.md) | GET | Reranks documents in Cohere for a search query. |
| [Tokenize](actions/tokenize.md) | GET | Tokenizes text into Cohere token IDs. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Embed Job](actions/cancel-embed-job.md) | PUT | Cancels an embed job in Cohere. |
| [Create Embed Job](actions/create-embed-job.md) | POST | Creates a new embed job in Cohere. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch from Cohere. |
| [Get Embed Job](actions/get-embed-job.md) | GET | Retrieves an embed job from Cohere. |
| [List Batches](actions/list-batches.md) | GET | Lists batch jobs in Cohere. |
| [List Embed Jobs](actions/list-embed-jobs.md) | GET | Lists embed jobs in Cohere. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Chat](actions/chat.md) | GET | Generates a chat response in Cohere. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Lists available AI models in Cohere. |

