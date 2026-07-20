# <img src="https://images.mindcloud.co/apps/icons/open-router_1773751178027.png" alt="OpenRouter logo" width="28" height="28"> OpenRouter: Universal API

Route AI requests across providers, discover models, and manage OpenRouter usage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openRouter/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openrouter.ai/
- **Vendor API docs:** https://openrouter.ai/docs/api/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current API Key](actions/get-current-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/get-current-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves user activity by endpoint from OpenRouter. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Current API Key](actions/get-current-api-key.md) | GET | Retrieves the current API key from OpenRouter. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in OpenRouter. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an existing API key from OpenRouter. |
| [Get API Key](actions/get-api-key.md) | GET | Retrieves a specific API key from OpenRouter. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves all API keys from OpenRouter. |
| [Update API Key](actions/update-api-key.md) | PUT | Updates an existing API key in OpenRouter. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in OpenRouter. |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves remaining account credits from OpenRouter. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embedding](actions/create-embedding.md) | POST | Creates a new embedding in OpenRouter. |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Model Endpoints](actions/list-model-endpoints.md) | GET | Retrieves endpoints for a specific model in OpenRouter. |
| [Preview ZDR Endpoints](actions/preview-zdr-endpoints.md) | GET | Previews ZDR-compatible model endpoints in OpenRouter. |

### Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation](actions/get-generation.md) | GET | Retrieves request and usage metadata for an OpenRouter generation. |

### Guardrail

| Action | Method | Description |
| --- | --- | --- |
| [Create Guardrail](actions/create-guardrail.md) | POST | Creates a new guardrail in OpenRouter. |
| [Delete Guardrail](actions/delete-guardrail.md) | DELETE | Deletes an existing guardrail from OpenRouter. |
| [Get Guardrail](actions/get-guardrail.md) | GET | Retrieves a specific guardrail from OpenRouter. |
| [List Guardrails](actions/list-guardrails.md) | GET | Retrieves all configured guardrails from OpenRouter. |
| [Update Guardrail](actions/update-guardrail.md) | PUT | Updates an existing guardrail in OpenRouter. |

### Guardrail Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Keys To Guardrail](actions/assign-keys-to-guardrail.md) | POST | Assigns API keys to a guardrail in OpenRouter. |
| [Assign Members To Guardrail](actions/assign-members-to-guardrail.md) | POST | Assigns members to a guardrail in OpenRouter. |
| [List Guardrail Key Assignments](actions/list-guardrail-key-assignments.md) | GET | Retrieves all guardrail-to-key assignments from OpenRouter. |
| [List Guardrail Key Assignments By Guardrail](actions/list-guardrail-key-assignments-by-guardrail.md) | GET | Retrieves key assignments for a specific guardrail in OpenRouter. |
| [List Guardrail Member Assignments](actions/list-guardrail-member-assignments.md) | GET | Retrieves all guardrail-to-member assignments from OpenRouter. |
| [List Guardrail Member Assignments By Guardrail](actions/list-guardrail-member-assignments-by-guardrail.md) | GET | Retrieves member assignments for a specific guardrail in OpenRouter. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a message response in OpenRouter. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available models and their properties from OpenRouter. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Embedding Models](actions/list-embedding-models.md) | GET | Retrieves available embedding models from OpenRouter. |
| [List User Models](actions/list-user-models.md) | GET | Retrieves models filtered by user settings from OpenRouter. |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Providers](actions/list-providers.md) | GET | Retrieves available model providers from OpenRouter. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a model response in OpenRouter. |

