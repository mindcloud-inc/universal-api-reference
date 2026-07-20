# LLMWhisperer: Native API Reference

A consolidated summary of LLMWhisperer's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_api/
- **API base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`

## Authentication

### API Key

Use your LLMWhisperer API key. Requests authenticate with the `unstract-key` header carrying the raw API key value.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
unstract-key: <apiKey>
```

[Official authentication documentation](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | `DELETE /whisper-manage-callback` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/) |
| [Get Extraction Details](actions/get-extraction-details.md) | `GET /whisper-detail` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_detail_api/) |
| [Get Extraction Status](actions/get-extraction-status.md) | `GET /whisper-status` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_status_api/) |
| [Get Highlight Lines](actions/get-highlight-lines.md) | `GET /highlights` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_highlighting_api/) |
| [Get Usage Metrics](actions/get-usage-metrics.md) | `GET /get-usage-info` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_usage_api/) |
| [Get Usage Stats](actions/get-usage-stats.md) | `GET /usage` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_usage_stats/) |
| [Get Webhook Details](actions/get-webhook-details.md) | `GET /whisper-manage-callback` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/) |
| [Register Webhook Endpoint](actions/register-webhook-endpoint.md) | `POST /whisper-manage-callback` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/) |
| [Retrieve Extracted Text](actions/retrieve-extracted-text.md) | `GET /whisper-retrieve` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_retrieve_api/) |
| [Start Extraction From URL](actions/start-extraction.md) | `POST /whisper` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_api/) |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | `PUT /whisper-manage-callback` | [docs](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/) |
