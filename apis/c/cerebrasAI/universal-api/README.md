# <img src="https://images.mindcloud.co/apps/icons/cerebras-icon-square_1776091600542.png" alt="Cerebras AI logo" width="28" height="28"> Cerebras AI: Universal API

Cerebras AI provides high-performance inference APIs for chat completions, text completions, model discovery, public model metadata, batch jobs, file management, metrics, and preview management operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cerebrasAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cerebras.ai/
- **Vendor API docs:** https://inference-docs.cerebras.ai/api-reference/versions

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | DELETE | Deletes a batch in Cerebras AI by cancelling it. |
| [Create Batch](actions/create-batch.md) | POST | Creates a batch in Cerebras AI. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches from Cerebras AI. |
| [Retrieve Batch](actions/retrieve-batch.md) | GET | Retrieves a batch from Cerebras AI. |

### Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Batch Results](actions/retrieve-batch-results.md) | GET | Retrieves batch results from Cerebras AI. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Cerebras AI. |

### Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Completion](actions/create-completion.md) | POST | Creates a completion in Cerebras AI. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoints](actions/list-endpoints.md) | GET | Retrieves endpoints from Cerebras AI. |
| [Retrieve Endpoint Status](actions/retrieve-endpoint-status.md) | GET | Retrieves endpoint status from Cerebras AI. |

### Endpoint Deployment

| Action | Method | Description |
| --- | --- | --- |
| [Deploy Model To Endpoint](actions/deploy-model-to-endpoint.md) | POST | Creates a model deployment to an endpoint in Cerebras AI. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Cerebras AI. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Cerebras AI. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from Cerebras AI. |
| [Upload File](actions/upload-file.md) | POST | Creates a file in Cerebras AI. |

### File Content

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve File Content](actions/retrieve-file-content.md) | GET | Retrieves file content from Cerebras AI. |

### Huggingface Public Model

| Action | Method | Description |
| --- | --- | --- |
| [List Public Models (HuggingFace)](actions/list-public-models-hugging-face.md) | GET | Retrieves HuggingFace-formatted public models from Cerebras AI. |
| [Retrieve Public Model (HuggingFace)](actions/retrieve-public-model-hugging-face.md) | GET | Retrieves a HuggingFace-formatted public model from Cerebras AI. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Metrics](actions/retrieve-metrics.md) | GET | Retrieves metrics from Cerebras AI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves models from Cerebras AI. |
| [Retrieve Model](actions/retrieve-model.md) | GET | Retrieves a model from Cerebras AI. |

### Model Architecture

| Action | Method | Description |
| --- | --- | --- |
| [List Model Architectures](actions/list-model-architectures.md) | GET | Retrieves model architectures from Cerebras AI. |

### Model Version

| Action | Method | Description |
| --- | --- | --- |
| [Delete Model Version](actions/delete-model-version.md) | DELETE | Deletes a model version from Cerebras AI. |
| [List Model Versions](actions/list-model-versions.md) | GET | Retrieves model versions from Cerebras AI. |
| [Update Model Version Aliases](actions/update-model-version-aliases.md) | PUT | Updates model version aliases in Cerebras AI. |
| [Upload Model Version](actions/upload-model-version.md) | POST | Creates a model version in Cerebras AI. |

### Model Version Status

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Model Version Status](actions/retrieve-model-version-status.md) | GET | Retrieves model version status from Cerebras AI. |

### Openrouter Public Model

| Action | Method | Description |
| --- | --- | --- |
| [List Public Models (OpenRouter)](actions/list-public-models-open-router.md) | GET | Retrieves OpenRouter-formatted public models from Cerebras AI. |
| [Retrieve Public Model (OpenRouter)](actions/retrieve-public-model-open-router.md) | GET | Retrieves an OpenRouter-formatted public model from Cerebras AI. |

### Public Model

| Action | Method | Description |
| --- | --- | --- |
| [List Public Models](actions/list-public-models.md) | GET | Retrieves public models from Cerebras AI. |
| [List Public Models (Generic Format)](actions/list-public-models-by-format.md) | GET | Retrieves public models from Cerebras AI by format. |
| [Retrieve Public Model](actions/retrieve-public-model.md) | GET | Retrieves a public model from Cerebras AI. |
| [Retrieve Public Model (Generic Format)](actions/retrieve-public-model-by-format.md) | GET | Retrieves a public model from Cerebras AI by format. |

