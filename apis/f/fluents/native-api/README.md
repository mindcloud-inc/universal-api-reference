# Fluents: Native API Reference

A consolidated summary of Fluents's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://docs.fluents.ai/api-reference
- **API base URL:** `https://api.fluents.ai/v1`

## Authentication

### API Key

Authenticate to Fluents with a Fluents environment API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.fluents.ai/product/how-to/environment)

## Pagination

Use `size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Buy Number](actions/buy-number.md) | `POST /numbers/buy` | [docs](https://docs.fluents.ai/api-reference/numbers/buy-number) |
| [Cancel Number](actions/cancel-number.md) | `POST /numbers/cancel` | [docs](https://docs.fluents.ai/api-reference/numbers/cancel-number) |
| [Create Account Connection](actions/create-account-connection.md) | `POST /account_connections/create` | [docs](https://docs.fluents.ai/api-reference/account_connections/create-account-connection) |
| [Create Action](actions/create-action.md) | `POST /actions/create` | [docs](https://docs.fluents.ai/api-reference/actions/create-action) |
| [Create Agent](actions/create-agent.md) | `POST /agents/create` | [docs](https://docs.fluents.ai/api-reference/agents/create-agent) |
| [Create Call](actions/create-call.md) | `POST /calls/create` | [docs](https://docs.fluents.ai/api-reference/calls/create-call) |
| [Create Prompt](actions/create-prompt.md) | `POST /prompts/create` | [docs](https://docs.fluents.ai/api-reference/prompts/create-prompt) |
| [Create Voice](actions/create-voice.md) | `POST /voices/create` | [docs](https://docs.fluents.ai/api-reference/voices/create-voice) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/create` | [docs](https://docs.fluents.ai/api-reference/webhooks/create-webhook) |
| [Delete Action](actions/delete-action.md) | `DELETE /actions/delete` | [docs](https://docs.fluents.ai/api-reference/actions) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /agents/delete` | [docs](https://docs.fluents.ai/api-reference/agents) |
| [Delete Prompt](actions/delete-prompt.md) | `DELETE /prompts/delete` | [docs](https://docs.fluents.ai/api-reference/prompts) |
| [Delete Voice](actions/delete-voice.md) | `DELETE /voices/delete` | [docs](https://docs.fluents.ai/api-reference/voices) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/delete` | [docs](https://docs.fluents.ai/api-reference/webhooks) |
| [Detach Number](actions/detach-number.md) | `POST /numbers/detach` | [docs](https://docs.fluents.ai/api-reference/numbers/detach-number) |
| [End Call](actions/end-call.md) | `POST /calls/end` | [docs](https://docs.fluents.ai/api-reference/calls/end-call) |
| [Get Account Connection](actions/get-account-connection.md) | `GET /account_connections` | [docs](https://docs.fluents.ai/api-reference/account_connections/get-account-connection) |
| [Get Action](actions/get-action.md) | `GET /actions` | [docs](https://docs.fluents.ai/api-reference/actions/get-action) |
| [Get Agent](actions/get-agent.md) | `GET /agents` | [docs](https://docs.fluents.ai/api-reference/agents/get-agent) |
| [Get Call](actions/get-call.md) | `GET /calls` | [docs](https://docs.fluents.ai/api-reference/calls/get-call) |
| [Get Number](actions/get-number.md) | `GET /numbers` | [docs](https://docs.fluents.ai/api-reference/numbers/get-number) |
| [Get Prompt](actions/get-prompt.md) | `GET /prompts` | [docs](https://docs.fluents.ai/api-reference/prompts/get-prompt) |
| [Get Recording](actions/get-recording.md) | `GET /calls/recording` | [docs](https://docs.fluents.ai/api-reference/calls/get-recording) |
| [Get Voice](actions/get-voice.md) | `GET /voices` | [docs](https://docs.fluents.ai/api-reference/voices/get-voice) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks` | [docs](https://docs.fluents.ai/api-reference/webhooks/get-webhook) |
| [Link Number](actions/link-number.md) | `POST /numbers/link` | [docs](https://docs.fluents.ai/api-reference/numbers/link-number) |
| [List Account Connections](actions/list-account-connections.md) | `GET /account_connections/list` | [docs](https://docs.fluents.ai/api-reference/account_connections/list-account-connections) |
| [List Actions](actions/list-actions.md) | `GET /actions/list` | [docs](https://docs.fluents.ai/api-reference/actions/list-actions) |
| [List Agents](actions/list-agents.md) | `GET /agents/list` | [docs](https://docs.fluents.ai/api-reference/agents/list-agents) |
| [List Available Numbers](actions/list-available-numbers.md) | `GET /numbers/available` | [docs](https://docs.fluents.ai/api-reference/numbers/list-available-numbers) |
| [List Calls](actions/list-calls.md) | `GET /calls/list` | [docs](https://docs.fluents.ai/api-reference/calls/list-calls) |
| [List Numbers](actions/list-numbers.md) | `GET /numbers/list` | [docs](https://docs.fluents.ai/api-reference/numbers/list-numbers) |
| [List Prompts](actions/list-prompts.md) | `GET /prompts/list` | [docs](https://docs.fluents.ai/api-reference/prompts/list-prompts) |
| [List Voices](actions/list-voices.md) | `GET /voices/list` | [docs](https://docs.fluents.ai/api-reference/voices/list-voices) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/list` | [docs](https://docs.fluents.ai/api-reference/webhooks/list-webhooks) |
| [Update Account Connection](actions/update-account-connection.md) | `POST /account_connections/update` | [docs](https://docs.fluents.ai/api-reference/account_connections/update-account-connection) |
| [Update Action](actions/update-action.md) | `POST /actions/update` | [docs](https://docs.fluents.ai/api-reference/actions/update-action) |
| [Update Agent](actions/update-agent.md) | `POST /agents/update` | [docs](https://docs.fluents.ai/api-reference/agents/update-agent) |
| [Update Number](actions/update-number.md) | `POST /numbers/update` | [docs](https://docs.fluents.ai/api-reference/numbers/update-number) |
| [Update Prompt](actions/update-prompt.md) | `POST /prompts/update` | [docs](https://docs.fluents.ai/api-reference/prompts/update-prompt) |
| [Update Voice](actions/update-voice.md) | `POST /voices/update` | [docs](https://docs.fluents.ai/api-reference/voices/update-voice) |
| [Update Webhook](actions/update-webhook.md) | `POST /webhooks/update` | [docs](https://docs.fluents.ai/api-reference/webhooks/update-webhook) |
