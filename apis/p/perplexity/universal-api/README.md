# <img src="https://images.mindcloud.co/apps/icons/perplexity_1776360244575.png" alt="Perplexity logo" width="28" height="28"> Perplexity: Universal API

Access Perplexity’s Search, Sonar, Agent, and Embeddings APIs for web search, grounded answers, multi-provider agent responses, and vector generation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/perplexity/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.perplexity.ai
- **Vendor API docs:** https://docs.perplexity.ai/docs/getting-started/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate Auth Token](actions/generate-auth-token.md) | POST | Creates an auth token in Perplexity. |
| [Revoke Auth Token](actions/revoke-auth-token.md) | DELETE | Revokes an auth token in Perplexity. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Contextualized Embeddings](actions/create-contextualized-embeddings.md) | POST | Creates contextualized embeddings from text in Perplexity. |
| [Create Embeddings](actions/create-embeddings.md) | POST | Creates embeddings from text in Perplexity. |
| [Search the Web](actions/search-the-web.md) | GET | Finds web search results in Perplexity by query. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Async Chat Completion](actions/create-async-chat-completion.md) | POST | Creates an async chat completion in Perplexity. |
| [Get Async Chat Completion](actions/get-async-chat-completion.md) | GET | Retrieves an async chat completion from Perplexity. |
| [List Async Chat Completions](actions/list-async-chat-completions.md) | GET | Retrieves async chat completions from Perplexity. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent Response](actions/create-agent-response.md) | POST | Creates an agent response in Perplexity. |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Perplexity. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available models from Perplexity. |

