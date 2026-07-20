# <img src="https://images.mindcloud.co/apps/icons/ollama_1775748591278.png" alt="Ollama logo" width="28" height="28"> Ollama: Universal API

Generate responses and inspect Ollama cloud models

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ollama/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ollama.com
- **Vendor API docs:** https://docs.ollama.com/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates an OpenAI-compatible chat completion in Ollama. |

### Chat Message

| Action | Method | Description |
| --- | --- | --- |
| [Generate Chat Message](actions/generate-chat-message.md) | POST | Generates the next chat message in Ollama. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Anthropic Message](actions/create-anthropic-message.md) | POST | Creates an Anthropic-compatible message in Ollama. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model (OpenAI Compatible)](actions/get-model-open-ai.md) | GET | Retrieves an OpenAI-compatible model from Ollama. |
| [List Models](actions/list-models.md) | GET | Retrieves available models from Ollama. |
| [List Models (OpenAI Compatible)](actions/list-models-open-ai.md) | GET | Retrieves OpenAI-compatible models from Ollama. |
| [Show Model Details](actions/show-model-details.md) | GET | Retrieves model details from Ollama. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates an OpenAI-compatible response in Ollama. |
| [Generate Response](actions/generate-response.md) | POST | Generates a response from an Ollama model. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Version](actions/get-version.md) | GET | Retrieves version information from Ollama. |

