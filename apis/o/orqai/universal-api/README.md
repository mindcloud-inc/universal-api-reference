# <img src="https://images.mindcloud.co/apps/icons/92824965_1776368710292.png" alt="Orq.ai logo" width="28" height="28"> Orq.ai: Universal API

Enterprise AI gateway and LLM collaboration platform for routing, observability, prompts, agents, knowledge, and model operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orqai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docs.orq.ai
- **Vendor API docs:** https://docs.orq.ai/docs/quick-start

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Orq.ai. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Orq.ai. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from Orq.ai. |
| [Retrieve Agent](actions/retrieve-agent.md) | GET | Retrieves an agent from Orq.ai. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Orq.ai. |

### Agent Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent Response](actions/create-agent-response.md) | POST | Creates an agent response in Orq.ai. |
| [Get Agent Response](actions/get-agent-response.md) | GET | Retrieves an agent response from Orq.ai. |

### Agent Task

| Action | Method | Description |
| --- | --- | --- |
| [Execute Agent Task](actions/execute-agent-task.md) | POST | Executes an agent task in Orq.ai. |
| [Run Agent With Configuration](actions/run-agent-with-configuration.md) | POST | Runs an agent with custom configuration in Orq.ai. |
| [Run Agent With Streaming Response](actions/run-agent-with-streaming-response.md) | POST | Runs an agent with streaming responses in Orq.ai. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | GET | Creates a chat completion in Orq.ai. |

### Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Completion](actions/create-completion.md) | GET | Creates a text completion in Orq.ai. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embeddings](actions/create-embeddings.md) | GET | Creates embeddings from input text in Orq.ai. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Uploads a file to Orq.ai. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Orq.ai. |
| [Download File Content](actions/download-file-content.md) | GET | Retrieves a presigned file download URL from Orq.ai. |
| [List Files](actions/list-files.md) | GET | Retrieves a list of files from Orq.ai. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from Orq.ai. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Orq.ai. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | GET | Creates an image in Orq.ai. |
| [Create Image Edit](actions/create-image-edit.md) | GET | Creates an image edit in Orq.ai. |
| [Create Image Variation](actions/create-image-variation.md) | GET | Creates an image variation in Orq.ai. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves a list of available models from Orq.ai. |

### Moderation

| Action | Method | Description |
| --- | --- | --- |
| [Create Moderation](actions/create-moderation.md) | GET | Creates a moderation result in Orq.ai. |

### Rerank

| Action | Method | Description |
| --- | --- | --- |
| [Create Rerank](actions/create-rerank.md) | GET | Creates reranked search results in Orq.ai. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a response in Orq.ai. |
| [Retrieve Response](actions/retrieve-response.md) | GET | Retrieves a response from Orq.ai. |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech](actions/create-speech.md) | GET | Creates speech audio from text in Orq.ai. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | GET | Creates an audio transcription in Orq.ai. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation](actions/create-translation.md) | GET | Creates an English audio translation in Orq.ai. |

