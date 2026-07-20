# Deep Infra: Native API Reference

A consolidated summary of Deep Infra's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.deepinfra.com/
- **API base URL:** `https://api.deepinfra.com`

## Authentication

### API Key

Authenticate DeepInfra API requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.deepinfra.com/account/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account GPU Limit](actions/get-account-gpu-limit.md) | `GET /v1/me/gpu_limit` | [docs](https://docs.deepinfra.com/api-reference/account/account-gpu-limit) |
| [Get Account Rate Limit](actions/get-account-rate-limit.md) | `GET /v1/me/rate_limit` | [docs](https://docs.deepinfra.com/api-reference/account/account-rate-limit) |
| [Get CLI Version](actions/get-cli-version.md) | `GET /cli/version` | [docs](https://docs.deepinfra.com/api-reference/utilities/cli-version) |
| [Get Current Account](actions/get-current-account.md) | `GET /v1/me` | [docs](https://docs.deepinfra.com/api-reference/account/me) |
| [Get Deployment GPU Availability](actions/get-deployment-gpu-availability.md) | `GET /deploy/llm/gpu_availability` | [docs](https://docs.deepinfra.com/api-reference/dedicated-models/deploy-gpu-availability) |
| [Get Deployment Stats](actions/get-deployment-stats.md) | `GET /deploy/:deploy_id/stats` | [docs](https://docs.deepinfra.com/api-reference/dedicated-models/deploy-stats) |
| [Get Deployment Status](actions/get-deployment-status.md) | `GET /deploy/:deploy_id` | [docs](https://docs.deepinfra.com/api-reference/dedicated-models/deploy-status) |
| [Get Live Metrics](actions/get-live-metrics.md) | `GET /v1/metrics/live` | [docs](https://docs.deepinfra.com/api-reference/logs-&-metrics/get-live-metrics) |
| [Get LoRA](actions/get-lora.md) | `GET /v1/lora/:lora_name` | [docs](https://docs.deepinfra.com/api-reference/lora-adapters/get-lora) |
| [Get LoRA Status](actions/get-lora-status.md) | `GET /v1/lora/:lora_name/status` | [docs](https://docs.deepinfra.com/api-reference/lora-adapters/get-lora-status) |
| [Get Model Family](actions/get-model-family.md) | `GET /model-families/:family_name` | [docs](https://docs.deepinfra.com/api-reference/models/model-family) |
| [Get Model Info](actions/get-model-info.md) | `GET /models/:model_name` | [docs](https://docs.deepinfra.com/api-reference/models/models-info) |
| [Get Model Schema](actions/get-model-schema.md) | `GET /models/:model_name/schema/:variantKey` | [docs](https://docs.deepinfra.com/api-reference/models/model-schema) |
| [Get Model Versions](actions/get-model-versions.md) | `GET /models/:model_name/versions` | [docs](https://docs.deepinfra.com/api-reference/models/model-versions) |
| [List Account Email Values](actions/list-account-email-values.md) | `GET /v1/me/emails` | [docs](https://docs.deepinfra.com/api-reference/account/account-email-values) |
| [List Deployment Models](actions/list-deployment-models.md) | `GET /models/deployment/list` | [docs](https://docs.deepinfra.com/api-reference/models/models-deployment-list) |
| [List Deployments](actions/list-deployments.md) | `GET /deploy/list` | [docs](https://docs.deepinfra.com/api-reference/dedicated-models/deploy-list-1) |
| [List Featured Models](actions/list-featured-models.md) | `GET /models/featured` | [docs](https://docs.deepinfra.com/api-reference/models/models-featured) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://docs.deepinfra.com/api-reference/files-&-batches/list-files) |
| [List LoRA Models](actions/list-lora-models.md) | `GET /models/lora/list` | [docs](https://docs.deepinfra.com/api-reference/models/models-lora-list) |
| [List Model Families](actions/list-model-families.md) | `GET /model-families/names` | [docs](https://docs.deepinfra.com/api-reference/models/model-families-names) |
| [List Model LoRAs](actions/list-model-loras.md) | `GET /v1/model/:model_name/loras` | [docs](https://docs.deepinfra.com/api-reference/lora-adapters/get-model-loras) |
| [List Models](actions/list-models.md) | `GET /models/list` | [docs](https://docs.deepinfra.com/api-reference/models/models-list) |
| [List OpenAI Batches](actions/list-open-ai-batches.md) | `GET /v1/batches` | [docs](https://docs.deepinfra.com/api-reference/files-&-batches/retrieve-openai-batches) |
| [List OpenAI Models](actions/list-open-ai-models.md) | `GET /v1/models` | [docs](https://docs.deepinfra.com/api-reference/models/openai-models.md) |
| [List OpenRouter Models](actions/list-open-router-models.md) | `GET /openrouter/models` | [docs](https://docs.deepinfra.com/api-reference/models/openrouter-models) |
| [List Private Models](actions/list-private-models.md) | `GET /models/private/list` | [docs](https://docs.deepinfra.com/api-reference/models/private-models-list) |
| [List User LoRAs](actions/list-user-loras.md) | `GET /v1/user/loras` | [docs](https://docs.deepinfra.com/api-reference/lora-adapters/get-user-loras) |
| [Query Deployment Logs](actions/query-deployment-logs.md) | `GET /v1/deployment_logs/query` | [docs](https://docs.deepinfra.com/api-reference/logs-&-metrics/deployment-logs-query) |
| [Query Inference Logs](actions/query-inference-logs.md) | `GET /v1/logs/query` | [docs](https://docs.deepinfra.com/api-reference/logs-&-metrics/logs-query) |
