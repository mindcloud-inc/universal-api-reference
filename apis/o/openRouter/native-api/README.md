# OpenRouter: Native API Reference

A consolidated summary of OpenRouter's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://openrouter.ai/docs/api/reference/overview
- **OpenAPI specification:** https://openrouter.ai/openapi.json
- **API base URL:** `https://openrouter.ai/api/v1/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://openrouter.ai/docs/api/reference/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Keys To Guardrail](actions/assign-keys-to-guardrail.md) | `POST /guardrails/:id/assignments/keys` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/bulk-assign-keys-to-guardrail) |
| [Assign Members To Guardrail](actions/assign-members-to-guardrail.md) | `POST /guardrails/:id/assignments/members` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/bulk-assign-members-to-guardrail) |
| [Create API Key](actions/create-api-key.md) | `POST /keys` | [docs](https://openrouter.ai/docs/api/api-reference/api-keys/create-keys) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /chat/completions` | [docs](https://openrouter.ai/docs/api/api-reference/chat/send-chat-completion-request) |
| [Create Embedding](actions/create-embedding.md) | `POST /embeddings` | [docs](https://openrouter.ai/docs/api/api-reference/embeddings/create-embeddings) |
| [Create Guardrail](actions/create-guardrail.md) | `POST /guardrails` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/create-guardrail) |
| [Create Message](actions/create-message.md) | `POST /messages` | [docs](https://openrouter.ai/docs/api/api-reference/anthropic-messages/create-messages) |
| [Create Response](actions/create-response.md) | `POST /responses` | [docs](https://openrouter.ai/docs/api/api-reference/responses/create-responses) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /keys/:hash` | [docs](https://openrouter.ai/docs/api/api-reference/api-keys/delete-keys) |
| [Delete Guardrail](actions/delete-guardrail.md) | `DELETE /guardrails/:id` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/delete-guardrail) |
| [Get Activity](actions/get-activity.md) | `GET /activity` | [docs](https://openrouter.ai/docs/api/api-reference/analytics/get-user-activity) |
| [Get API Key](actions/get-api-key.md) | `GET /keys/:hash` | [docs](https://openrouter.ai/docs/api/api-reference/api-keys/get-key) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://openrouter.ai/docs/api/api-reference/credits/get-credits) |
| [Get Current API Key](actions/get-current-api-key.md) | `GET /key` | [docs](https://openrouter.ai/docs/api/api-reference/api-keys/get-current-key) |
| [Get Generation](actions/get-generation.md) | `GET /generation` | [docs](https://openrouter.ai/docs/api/api-reference/generations/get-generation) |
| [Get Guardrail](actions/get-guardrail.md) | `GET /guardrails/:id` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/get-guardrail) |
| [List API Keys](actions/list-api-keys.md) | `GET /keys` | [docs](https://openrouter.ai/docs/api/api-reference/api-keys/list) |
| [List Embedding Models](actions/list-embedding-models.md) | `GET /embeddings/models` | [docs](https://openrouter.ai/docs/api/api-reference/embeddings/list-embeddings-models) |
| [List Guardrail Key Assignments](actions/list-guardrail-key-assignments.md) | `GET /guardrails/assignments/keys` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/list-key-assignments) |
| [List Guardrail Key Assignments By Guardrail](actions/list-guardrail-key-assignments-by-guardrail.md) | `GET /guardrails/:id/assignments/keys` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/list-guardrail-key-assignments) |
| [List Guardrail Member Assignments](actions/list-guardrail-member-assignments.md) | `GET /guardrails/assignments/members` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/list-member-assignments) |
| [List Guardrail Member Assignments By Guardrail](actions/list-guardrail-member-assignments-by-guardrail.md) | `GET /guardrails/:id/assignments/members` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/list-guardrail-member-assignments) |
| [List Guardrails](actions/list-guardrails.md) | `GET /guardrails` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/list-guardrails) |
| [List Model Endpoints](actions/list-model-endpoints.md) | `GET /models/:author/:slug/endpoints` | [docs](https://openrouter.ai/docs/api/api-reference/endpoints/list-endpoints) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://openrouter.ai/docs/api/api-reference/models/get-models) |
| [List Providers](actions/list-providers.md) | `GET /providers` | [docs](https://openrouter.ai/docs/api/api-reference/providers/list-providers) |
| [List User Models](actions/list-user-models.md) | `GET /models/user` | [docs](https://openrouter.ai/docs/api/api-reference/models/list-models-user) |
| [Preview ZDR Endpoints](actions/preview-zdr-endpoints.md) | `GET /endpoints/zdr` | [docs](https://openrouter.ai/docs/api/api-reference/endpoints/list-endpoints-zdr) |
| [Update API Key](actions/update-api-key.md) | `PATCH /keys/:hash` | [docs](https://openrouter.ai/docs/api/api-reference/api-keys/update-keys) |
| [Update Guardrail](actions/update-guardrail.md) | `PATCH /guardrails/:id` | [docs](https://openrouter.ai/docs/api/api-reference/guardrails/update-guardrail) |
