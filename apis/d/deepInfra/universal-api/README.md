# <img src="https://images.mindcloud.co/apps/icons/deep-infra_1776880393878.png" alt="Deep Infra logo" width="28" height="28"> Deep Infra: Universal API

Run AI inference and manage DeepInfra models

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deepInfra/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://deepinfra.com/
- **Vendor API docs:** https://docs.deepinfra.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List OpenAI Models](actions/list-open-ai-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/list-open-ai-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET |  |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [List OpenAI Batches](actions/list-open-ai-batches.md) | GET |  |

### Cli Version

| Action | Method | Description |
| --- | --- | --- |
| [Get CLI Version](actions/get-cli-version.md) | GET |  |

### Deployment

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Status](actions/get-deployment-status.md) | GET |  |
| [List Deployments](actions/list-deployments.md) | GET |  |

### Deployment Log

| Action | Method | Description |
| --- | --- | --- |
| [Query Deployment Logs](actions/query-deployment-logs.md) | GET |  |

### Deployment Model

| Action | Method | Description |
| --- | --- | --- |
| [List Deployment Models](actions/list-deployment-models.md) | GET |  |

### Deployment Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Stats](actions/get-deployment-stats.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [List Account Email Values](actions/list-account-email-values.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET |  |

### Gpu Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment GPU Availability](actions/get-deployment-gpu-availability.md) | GET |  |

### Gpu Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Account GPU Limit](actions/get-account-gpu-limit.md) | GET |  |

### Inference Log

| Action | Method | Description |
| --- | --- | --- |
| [Query Inference Logs](actions/query-inference-logs.md) | GET |  |

### Lora Adapter

| Action | Method | Description |
| --- | --- | --- |
| [Get LoRA](actions/get-lora.md) | GET |  |
| [Get LoRA Status](actions/get-lora-status.md) | GET |  |
| [List Model LoRAs](actions/list-model-loras.md) | GET |  |
| [List User LoRAs](actions/list-user-loras.md) | GET |  |

### Lora Model

| Action | Method | Description |
| --- | --- | --- |
| [List LoRA Models](actions/list-lora-models.md) | GET |  |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Metrics](actions/get-live-metrics.md) | GET |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Info](actions/get-model-info.md) | GET |  |
| [List Featured Models](actions/list-featured-models.md) | GET |  |
| [List Models](actions/list-models.md) | GET |  |
| [List OpenAI Models](actions/list-open-ai-models.md) | GET |  |
| [List OpenRouter Models](actions/list-open-router-models.md) | GET |  |

### Model Family

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Family](actions/get-model-family.md) | GET |  |
| [List Model Families](actions/list-model-families.md) | GET |  |

### Model Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Schema](actions/get-model-schema.md) | GET |  |

### Model Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Versions](actions/get-model-versions.md) | GET |  |

### Private Model

| Action | Method | Description |
| --- | --- | --- |
| [List Private Models](actions/list-private-models.md) | GET |  |

### Rate Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Rate Limit](actions/get-account-rate-limit.md) | GET |  |

