# Hume: Native API Reference

A consolidated summary of Hume's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://dev.hume.ai/docs
- **OpenAPI specification:** https://dev.hume.ai/openapi.json
- **API base URL:** `https://api.hume.ai`

## Authentication

### API Key

Authenticate requests with a Hume API key sent in the X-Hume-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.hume.ai/docs/introduction/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create config](actions/create-config.md) | `POST /v0/evi/configs` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/create-config) |
| [Create config version](actions/create-config-version.md) | `POST /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/create-config-version) |
| [Create prompt](actions/create-prompt.md) | `POST /v0/evi/prompts` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/create-prompt) |
| [Create prompt version](actions/create-prompt-version.md) | `POST /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/create-prompt-version) |
| [Create tool](actions/create-tool.md) | `POST /v0/evi/tools` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/create-tool) |
| [Create tool version](actions/create-tool-version.md) | `POST /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/create-tool-version) |
| [Delete config](actions/delete-config.md) | `DELETE /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/delete-config) |
| [Delete config version](actions/delete-config-version.md) | `DELETE /v0/evi/configs/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/delete-config-version) |
| [Delete prompt](actions/delete-prompt.md) | `DELETE /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/delete-prompt) |
| [Delete prompt version](actions/delete-prompt-version.md) | `DELETE /v0/evi/prompts/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/delete-prompt-version) |
| [Delete tool](actions/delete-tool.md) | `DELETE /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/delete-tool) |
| [Delete tool version](actions/delete-tool-version.md) | `DELETE /v0/evi/tools/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/delete-tool-version) |
| [Get chat audio](actions/get-chat-audio.md) | `GET /v0/evi/chats/:id/audio` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chats/get-audio) |
| [Get chat group](actions/get-chat-group.md) | `GET /v0/evi/chat_groups/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chat-groups/get-chat-group) |
| [Get chat group audio](actions/get-chat-group-audio.md) | `GET /v0/evi/chat_groups/:id/audio` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chat-groups/get-audio) |
| [Get config version](actions/get-config-version.md) | `GET /v0/evi/configs/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/get-config-version) |
| [Get job artifacts](actions/get-job-artifacts.md) | `GET /v0/batch/jobs/:id/artifacts` | [docs](https://dev.hume.ai/reference/expression-measurement-api/batch/get-job-artifacts) |
| [Get job details](actions/get-job-details.md) | `GET /v0/batch/jobs/:id` | [docs](https://dev.hume.ai/reference/expression-measurement-api/batch/get-job-details) |
| [Get job predictions](actions/get-job-predictions.md) | `GET /v0/batch/jobs/:id/predictions` | [docs](https://dev.hume.ai/reference/expression-measurement-api/batch/get-job-predictions) |
| [Get prompt version](actions/get-prompt-version.md) | `GET /v0/evi/prompts/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/get-prompt-version) |
| [Get tool version](actions/get-tool-version.md) | `GET /v0/evi/tools/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/get-tool-version) |
| [List chat events](actions/list-chat-events.md) | `GET /v0/evi/chats/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chats/list-chat-events) |
| [List chat group events](actions/list-chat-group-events.md) | `GET /v0/evi/chat_groups/:id/events` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chat-groups/list-chat-group-events) |
| [List chat groups](actions/list-chat-groups.md) | `GET /v0/evi/chat_groups` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chat-groups/list-chat-groups) |
| [List chats](actions/list-chats.md) | `GET /v0/evi/chats` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/chats/list-chats) |
| [List config versions](actions/list-config-versions.md) | `GET /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/list-config-versions) |
| [List configs](actions/list-configs.md) | `GET /v0/evi/configs` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/list-configs) |
| [List jobs](actions/list-jobs.md) | `GET /v0/batch/jobs` | [docs](https://dev.hume.ai/reference/expression-measurement-api/batch/list-jobs) |
| [List prompt versions](actions/list-prompt-versions.md) | `GET /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/list-prompt-versions) |
| [List prompts](actions/list-prompts.md) | `GET /v0/evi/prompts` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/list-prompts) |
| [List tool versions](actions/list-tool-versions.md) | `GET /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/list-tool-versions) |
| [List tools](actions/list-tools.md) | `GET /v0/evi/tools` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/list-tools) |
| [List voices](actions/list-voices.md) | `GET /v0/tts/voices` | [docs](https://dev.hume.ai/reference/voices/list) |
| [Synthesize speech](actions/synthesize-speech.md) | `POST /v0/tts` | [docs](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-json) |
| [Update config description](actions/update-config-description.md) | `PATCH /v0/evi/configs/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/update-config-description) |
| [Update config name](actions/update-config-name.md) | `PATCH /v0/evi/configs/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/configs/update-config-name) |
| [Update prompt description](actions/update-prompt-description.md) | `PATCH /v0/evi/prompts/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/update-prompt-description) |
| [Update prompt name](actions/update-prompt-name.md) | `PATCH /v0/evi/prompts/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/update-prompt-name) |
| [Update tool description](actions/update-tool-description.md) | `PATCH /v0/evi/tools/:id/version/:version` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/update-tool-description) |
| [Update tool name](actions/update-tool-name.md) | `PATCH /v0/evi/tools/:id` | [docs](https://dev.hume.ai/reference/speech-to-speech-evi/tools/update-tool-name) |
