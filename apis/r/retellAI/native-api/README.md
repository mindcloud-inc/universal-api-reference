# Retell AI: Native API Reference

A consolidated summary of Retell AI's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.retellai.com/api-references
- **OpenAPI specification:** https://docs.retellai.com/openapi.yaml
- **API base URL:** `https://api.retellai.com`

## Authentication

### API Key

Connect Retell AI with a Retell API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.retellai.com/accounts/api-keys-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `pagination_key` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Knowledge Base Sources](actions/add-knowledge-base-sources.md) | `POST /add-knowledge-base-sources/{knowledge_base_id}` | [docs](https://docs.retellai.com/api-references/add-knowledge-base-sources) |
| [Create Chat](actions/create-chat.md) | `POST /create-chat` | [docs](https://docs.retellai.com/api-references/create-chat) |
| [Create Chat Agent](actions/create-chat-agent.md) | `POST /create-chat-agent` | [docs](https://docs.retellai.com/api-references/create-chat-agent) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /create-knowledge-base` | [docs](https://docs.retellai.com/api-references/create-knowledge-base) |
| [Create Phone Call](actions/create-phone-call.md) | `POST /v2/create-phone-call` | [docs](https://docs.retellai.com/api-references/create-phone-call) |
| [Create Retell LLM](actions/create-retell-llm.md) | `POST /create-retell-llm` | [docs](https://docs.retellai.com/api-references/create-retell-llm) |
| [Create Voice Agent](actions/create-voice-agent.md) | `POST /create-agent` | [docs](https://docs.retellai.com/api-references/create-agent) |
| [Create Web Call](actions/create-web-call.md) | `POST /v2/create-web-call` | [docs](https://docs.retellai.com/api-references/create-web-call) |
| [End Chat](actions/end-chat.md) | `PATCH /end-chat/{chat_id}` | [docs](https://docs.retellai.com/api-references/end-chat) |
| [Get Call](actions/get-call.md) | `GET /v2/get-call/{call_id}` | [docs](https://docs.retellai.com/api-references/get-call) |
| [Get Chat](actions/get-chat.md) | `GET /get-chat/{chat_id}` | [docs](https://docs.retellai.com/api-references/get-chat) |
| [Get Chat Agent](actions/get-chat-agent.md) | `GET /get-chat-agent/{agent_id}` | [docs](https://docs.retellai.com/api-references/get-chat-agent) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET /get-knowledge-base/{knowledge_base_id}` | [docs](https://docs.retellai.com/api-references/get-knowledge-base) |
| [Get Phone Number](actions/get-phone-number.md) | `GET /get-phone-number/{phone_number}` | [docs](https://docs.retellai.com/api-references/get-phone-number) |
| [Get Retell LLM](actions/get-retell-llm.md) | `GET /get-retell-llm/{llm_id}` | [docs](https://docs.retellai.com/api-references/get-retell-llm) |
| [Get Voice Agent](actions/get-voice-agent.md) | `GET /get-agent/{agent_id}` | [docs](https://docs.retellai.com/api-references/get-agent) |
| [List Calls](actions/list-calls.md) | `POST /v2/list-calls` | [docs](https://docs.retellai.com/api-references/list-calls) |
| [List Chat](actions/list-chat.md) | `GET /list-chat` | [docs](https://docs.retellai.com/api-references/list-chat) |
| [List Chat Agents](actions/list-chat-agents.md) | `GET /list-chat-agents` | [docs](https://docs.retellai.com/api-references/list-chat-agents) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /list-knowledge-bases` | [docs](https://docs.retellai.com/api-references/list-knowledge-bases) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /v2/list-phone-numbers` | [docs](https://docs.retellai.com/api-references/list-phone-numbers) |
| [List Retell LLMs](actions/list-retell-llms.md) | `GET /list-retell-llms` | [docs](https://docs.retellai.com/api-references/list-retell-llms) |
| [List Voice Agents](actions/list-voice-agents.md) | `GET /list-agents` | [docs](https://docs.retellai.com/api-references/list-agents) |
| [List Voices](actions/list-voices.md) | `GET /list-voices` | [docs](https://docs.retellai.com/api-references/list-voices) |
| [Publish Agent](actions/publish-agent.md) | `POST /publish-agent/{agent_id}` | [docs](https://docs.retellai.com/api-references/publish-agent) |
| [Publish Chat Agent](actions/publish-chat-agent.md) | `POST /publish-chat-agent/{agent_id}` | [docs](https://docs.retellai.com/api-references/publish-chat-agent) |
| [Update Chat Agent](actions/update-chat-agent.md) | `PATCH /update-chat-agent/{agent_id}` | [docs](https://docs.retellai.com/api-references/update-chat-agent) |
| [Update Phone Number](actions/update-phone-number.md) | `PATCH /update-phone-number/{phone_number}` | [docs](https://docs.retellai.com/api-references/update-phone-number) |
| [Update Retell LLM](actions/update-retell-llm.md) | `PATCH /update-retell-llm/{llm_id}` | [docs](https://docs.retellai.com/api-references/update-retell-llm) |
| [Update Voice Agent](actions/update-voice-agent.md) | `PATCH /update-agent/{agent_id}` | [docs](https://docs.retellai.com/api-references/update-agent) |
