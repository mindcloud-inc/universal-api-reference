# Mindee: Native API Reference

A consolidated summary of Mindee's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.mindee.com/integrations/api-reference
- **OpenAPI specification:** https://api-v2.mindee.net/openapi.json
- **API base URL:** `https://api-v2.mindee.net`

## Authentication

### API Key

Authenticate Mindee requests with an organization API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.mindee.com/integrations/api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Classification Result](actions/get-classification-result.md) | `GET /v2/products/classification/results/:inference_id` | [docs](https://docs.mindee.com/integrations/api-reference/classification-models) |
| [Get Crop Result](actions/get-crop-result.md) | `GET /v2/products/crop/results/:inference_id` | [docs](https://docs.mindee.com/integrations/api-reference/crop-models) |
| [Get Extraction Result](actions/get-extraction-result.md) | `GET /v2/products/extraction/results/:inference_id` | [docs](https://docs.mindee.com/integrations/api-reference/extraction-models) |
| [Get Job Status](actions/get-job-status.md) | `GET /v2/jobs/:job_id` | [docs](https://docs.mindee.com/integrations/api-reference) |
| [Get OCR Result](actions/get-ocr-result.md) | `GET /v2/products/ocr/results/:inference_id` | [docs](https://docs.mindee.com/integrations/api-reference/ocr-models) |
| [Get Split Result](actions/get-split-result.md) | `GET /v2/products/split/results/:inference_id` | [docs](https://docs.mindee.com/integrations/api-reference/split-models) |
| [Start Classification Job From URL](actions/start-classification-job-from-url.md) | `POST /v2/products/classification/enqueue` | [docs](https://docs.mindee.com/integrations/api-reference/classification-models) |
| [Start Crop Job From URL](actions/start-crop-job-from-url.md) | `POST /v2/products/crop/enqueue` | [docs](https://docs.mindee.com/integrations/api-reference/crop-models) |
| [Start Extraction Job From URL](actions/start-extraction-job-from-url.md) | `POST /v2/products/extraction/enqueue` | [docs](https://docs.mindee.com/integrations/api-reference/extraction-models) |
| [Start OCR Job From URL](actions/start-ocr-job-from-url.md) | `POST /v2/products/ocr/enqueue` | [docs](https://docs.mindee.com/integrations/api-reference/ocr-models) |
| [Start Split Job From URL](actions/start-split-job-from-url.md) | `POST /v2/products/split/enqueue` | [docs](https://docs.mindee.com/integrations/api-reference/split-models) |
