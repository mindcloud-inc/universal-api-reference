# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-sea-lion-ai-48x48_1776344521073.png" alt="SEA-LION AI Playground logo" width="28" height="28"> SEA-LION AI Playground: Universal API

Generate, rank, and analyze content with SEA-LION models

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sEALIONAIPlaygroundAPI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sea-lion.ai
- **Vendor API docs:** https://docs.sea-lion.ai/guides/inferencing/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST |  |
| [Create Embedding](actions/create-embedding.md) | POST |  |
| [Create Response](actions/create-response.md) | POST |  |
| [Create Text Completion](actions/create-text-completion.md) | POST |  |
| [Rerank Documents](actions/rerank-documents.md) | GET |  |

