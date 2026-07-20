# <img src="https://images.mindcloud.co/apps/icons/fal-ai-icon-1_1781893709215.png" alt="fal.ai logo" width="28" height="28"> fal.ai: Universal API

fal.ai Platform APIs for model metadata, usage, serverless operations, compute instances, API key management, workflow metadata, account reporting, and platform metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/falai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fal.ai
- **Vendor API docs:** https://fal.ai/docs/api-reference/platform-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Platform Metadata](actions/get-platform-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-platform-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics](actions/get-analytics.md) | GET | Retrieves model endpoint analytics from fal.ai. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates an API key in fal.ai. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an API key from fal.ai. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves workspace API keys from fal.ai. |

### Billing Event

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Events](actions/list-billing-events.md) | GET | Retrieves billing event records from fal.ai. |

### Billing Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Billing](actions/get-account-billing.md) | GET | Retrieves account billing details from fal.ai. |

### Compute Instance

| Action | Method | Description |
| --- | --- | --- |
| [Create Compute Instance](actions/create-compute-instance.md) | POST | Creates a compute instance in fal.ai. |
| [Delete Compute Instance](actions/delete-compute-instance.md) | DELETE | Deletes a compute instance from fal.ai. |
| [Get Compute Instance](actions/get-compute-instance.md) | GET | Retrieves compute instance details from fal.ai. |
| [List Compute Instances](actions/list-compute-instances.md) | GET | Retrieves workspace compute instances from fal.ai. |

### Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Cost](actions/estimate-cost.md) | POST | Estimates costs for fal.ai model endpoints. |

### Focus Report

| Action | Method | Description |
| --- | --- | --- |
| [Get FOCUS Report](actions/get-focus-report.md) | GET | Retrieves a FOCUS billing report from fal.ai. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Finds model endpoints available in fal.ai. |

### Model Access Controls Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Access Controls](actions/get-model-access-controls.md) | GET | Retrieves a model access controls report from fal.ai. |

### Platform Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Platform Metadata](actions/get-platform-metadata.md) | GET | Retrieves fal.ai platform metadata and webhook IP ranges. |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Pricing](actions/get-pricing.md) | GET | Retrieves model endpoint pricing from fal.ai. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [List Requests By Endpoint](actions/list-requests-by-endpoint.md) | GET | Retrieves requests for fal.ai model endpoints. |
| [Search Requests](actions/search-requests.md) | GET |  |

### Request Payload

| Action | Method | Description |
| --- | --- | --- |
| [Delete Request Payloads](actions/delete-request-payloads.md) | DELETE | Deletes fal.ai request payloads and output files. |

### Serverless File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Retrieves a file from fal.ai storage. |
| [List Directory Files](actions/list-directory-files.md) | GET | Retrieves storage files from a fal.ai directory. |
| [List Root Files](actions/list-root-files.md) | GET | Retrieves root storage files from fal.ai. |
| [Upload File From URL](actions/upload-file-from-url.md) | POST | Creates a fal.ai storage file from a URL. |
| [Upload Local File](actions/upload-local-file.md) | POST | Creates a fal.ai storage file from a local upload. |

### Serverless Log Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Logs History](actions/get-logs-history.md) | GET | Retrieves historical serverless logs from fal.ai. |

### Serverless Log Stream

| Action | Method | Description |
| --- | --- | --- |
| [Stream Logs](actions/stream-logs.md) | GET | Streams live serverless logs from fal.ai. |

### Serverless Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Serverless Metrics](actions/get-serverless-metrics.md) | GET | Retrieves Prometheus-compatible serverless metrics from fal.ai. |

### Serverless Queue

| Action | Method | Description |
| --- | --- | --- |
| [Flush Application Queue](actions/flush-application-queue.md) | DELETE | Deletes pending requests from a fal.ai application queue. |
| [Get Queue Size](actions/get-queue-size.md) | GET | Retrieves queue size for a fal.ai application. |

### Serverless Request

| Action | Method | Description |
| --- | --- | --- |
| [List Serverless Requests By Endpoint](actions/list-serverless-requests-by-endpoint.md) | GET | Retrieves requests for fal.ai serverless endpoints. |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves workspace model usage records from fal.ai. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves detailed workflow information from fal.ai. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves authenticated user workflows from fal.ai. |

