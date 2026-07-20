# fal.ai: Native API Reference

A consolidated summary of fal.ai's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://fal.ai/docs/api-reference/platform-apis
- **OpenAPI specification:** https://api.fal.ai/v1/openapi.json
- **API base URL:** `https://api.fal.ai/v1`

## Authentication

### API Key

fal.ai Platform APIs require an API key sent as Authorization: Key <token>.

### Credentials

- **API Key:** `apiKey` · required · Your fal.ai admin API key. The runtime sends it as Authorization: Key <api key>.

[Official authentication documentation](https://fal.ai/docs/api-reference/platform-apis/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | `POST /keys` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Create Compute Instance](actions/create-compute-instance.md) | `POST /compute/instances` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /keys/:keyId` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Delete Compute Instance](actions/delete-compute-instance.md) | `DELETE /compute/instances/:id` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Delete Request Payloads](actions/delete-request-payloads.md) | `DELETE /models/requests/:requestId/payloads` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Download File](actions/download-file.md) | `GET /serverless/files/file/:file` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Estimate Cost](actions/estimate-cost.md) | `POST /models/pricing/estimate` | [docs](https://fal.ai/docs/platform-apis/v1/models/pricing/estimate) |
| [Flush Application Queue](actions/flush-application-queue.md) | `DELETE /serverless/apps/:owner/:name/queue` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Account Billing](actions/get-account-billing.md) | `GET /account/billing` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Analytics](actions/get-analytics.md) | `GET /models/analytics` | [docs](https://fal.ai/docs/platform-apis/v1/models/analytics) |
| [Get Compute Instance](actions/get-compute-instance.md) | `GET /compute/instances/:id` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get FOCUS Report](actions/get-focus-report.md) | `GET /account/focus` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Logs History](actions/get-logs-history.md) | `POST /serverless/logs/history` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Model Access Controls](actions/get-model-access-controls.md) | `GET /account/model-access-controls` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Platform Metadata](actions/get-platform-metadata.md) | `GET /meta` | [docs](https://fal.ai/docs/platform-apis/v1/meta/get) |
| [Get Pricing](actions/get-pricing.md) | `GET /models/pricing` | [docs](https://fal.ai/docs/platform-apis/v1/models/pricing) |
| [Get Queue Size](actions/get-queue-size.md) | `GET /serverless/apps/:owner/:name/queue` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Serverless Metrics](actions/get-serverless-metrics.md) | `GET /serverless/metrics` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Get Usage](actions/get-usage.md) | `GET /models/usage` | [docs](https://fal.ai/docs/platform-apis/v1/models/usage) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:username/:workflowName` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [List API Keys](actions/list-api-keys.md) | `GET /keys` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [List Billing Events](actions/list-billing-events.md) | `GET /models/billing-events` | [docs](https://fal.ai/docs/platform-apis/v1/models/billing-events) |
| [List Compute Instances](actions/list-compute-instances.md) | `GET /compute/instances` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [List Directory Files](actions/list-directory-files.md) | `GET /serverless/files/list/:dir` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://fal.ai/docs/platform-apis/v1/models/search) |
| [List Requests By Endpoint](actions/list-requests-by-endpoint.md) | `GET /models/requests/by-endpoint` | [docs](https://fal.ai/docs/platform-apis/v1/models/requests/by-endpoint) |
| [List Root Files](actions/list-root-files.md) | `GET /serverless/files/list` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [List Serverless Requests By Endpoint](actions/list-serverless-requests-by-endpoint.md) | `GET /serverless/requests/by-endpoint` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Search Requests](actions/search-requests.md) | `GET /models/requests/search` | [docs](https://fal.ai/docs/platform-apis/v1/models/requests/search) |
| [Stream Logs](actions/stream-logs.md) | `POST /serverless/logs/stream` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Upload File From URL](actions/upload-file-from-url.md) | `POST /serverless/files/file/url/:file` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
| [Upload Local File](actions/upload-local-file.md) | `POST /serverless/files/file/local/:targetPath` | [docs](https://fal.ai/docs/api-reference/platform-apis) |
