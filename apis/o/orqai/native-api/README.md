# Orq.ai: Native API Reference

A consolidated summary of Orq.ai's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.orq.ai/docs/quick-start
- **API base URL:** `https://api.orq.ai`

## Authentication

### API Key

Connect with a Workspace API key from Orq.ai.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.orq.ai/docs/administer/api-keys)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /v2/agents` | [docs](https://docs.orq.ai/reference/agents/create-agent) |
| [Create Agent Response](actions/create-agent-response.md) | `POST /v2/agents/[:agent_key]/responses` | [docs](https://docs.orq.ai/reference/agents/create-response) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v2/router/chat/completions` | [docs](https://docs.orq.ai/reference/chat/create-chat-completion) |
| [Create Completion](actions/create-completion.md) | `POST /v2/router/completions` | [docs](https://docs.orq.ai/reference/completions/create-completion) |
| [Create Embeddings](actions/create-embeddings.md) | `POST /v2/router/embeddings` | [docs](https://docs.orq.ai/reference/embeddings/create-embeddings) |
| [Create File](actions/create-file.md) | `POST /v2/files` | [docs](https://docs.orq.ai/reference/files/create-file) |
| [Create Image](actions/create-image.md) | `POST /v2/router/images/generations` | [docs](https://docs.orq.ai/reference/images/create-image) |
| [Create Image Edit](actions/create-image-edit.md) | `POST /v2/router/images/edits` | [docs](https://docs.orq.ai/reference/images/create-image-edit) |
| [Create Image Variation](actions/create-image-variation.md) | `POST /v2/router/images/variations` | [docs](https://docs.orq.ai/reference/images/create-image-variation) |
| [Create Moderation](actions/create-moderation.md) | `POST /v2/router/moderations` | [docs](https://docs.orq.ai/reference/moderations/create-moderation) |
| [Create Rerank](actions/create-rerank.md) | `POST /v2/router/rerank` | [docs](https://docs.orq.ai/reference/rerank/create-rerank) |
| [Create Response](actions/create-response.md) | `POST /v3/router/responses` | [docs](https://docs.orq.ai/reference/responses/v3-create-response) |
| [Create Speech](actions/create-speech.md) | `POST /v2/router/audio/speech` | [docs](https://docs.orq.ai/reference/audio/create-speech) |
| [Create Transcription](actions/create-transcription.md) | `POST /v2/router/audio/transcriptions` | [docs](https://docs.orq.ai/reference/audio/create-transcription) |
| [Create Translation](actions/create-translation.md) | `POST /v2/router/audio/translations` | [docs](https://docs.orq.ai/reference/audio/create-translation) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /v2/agents/[:agent_key]` | [docs](https://docs.orq.ai/reference/agents/delete-agent) |
| [Delete File](actions/delete-file.md) | `DELETE /v2/files/[:file_id]` | [docs](https://docs.orq.ai/reference/files/delete-file) |
| [Download File Content](actions/download-file-content.md) | `GET /v2/files/[:file_id_or_path]/content` | [docs](https://docs.orq.ai/reference/files/download-file-content) |
| [Execute Agent Task](actions/execute-agent-task.md) | `POST /v2/agents/[:agent_key]/task` | [docs](https://docs.orq.ai/reference/agents/execute-an-agent-task) |
| [Get Agent Response](actions/get-agent-response.md) | `GET /v2/agents/[:agent_key]/responses/[:task_id]` | [docs](https://docs.orq.ai/reference/agents/get-response) |
| [List Agents](actions/list-agents.md) | `GET /v2/agents` | [docs](https://docs.orq.ai/reference/agents/list-agents) |
| [List Files](actions/list-files.md) | `GET /v2/files` | [docs](https://docs.orq.ai/reference/files/list-all-files) |
| [List Models](actions/list-models.md) | `GET /v2/models` | [docs](https://docs.orq.ai/reference/models/list-models) |
| [Retrieve Agent](actions/retrieve-agent.md) | `GET /v2/agents/[:agent_key]` | [docs](https://docs.orq.ai/reference/agents/retrieve-agent) |
| [Retrieve File](actions/retrieve-file.md) | `GET /v2/files/[:file_id]` | [docs](https://docs.orq.ai/reference/files/retrieve-a-file) |
| [Retrieve Response](actions/retrieve-response.md) | `GET /v3/router/responses/[:response_id]` | [docs](https://docs.orq.ai/reference/responses/v3-retrieve-response) |
| [Run Agent With Configuration](actions/run-agent-with-configuration.md) | `POST /v2/agents/run` | [docs](https://docs.orq.ai/reference/agents/run-an-agent-with-configuration) |
| [Run Agent With Streaming Response](actions/run-agent-with-streaming-response.md) | `POST /v2/agents/stream-run` | [docs](https://docs.orq.ai/reference/agents/run-agent-with-streaming-response) |
| [Update Agent](actions/update-agent.md) | `PATCH /v2/agents/[:agent_key]` | [docs](https://docs.orq.ai/reference/agents/update-agent) |
| [Update File](actions/update-file.md) | `PATCH /v2/files/[:file_id]` | [docs](https://docs.orq.ai/reference/files/update-file) |
