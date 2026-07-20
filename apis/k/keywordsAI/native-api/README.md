# Keywords AI: Native API Reference

A consolidated summary of Keywords AI's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://www.respan.ai/docs/apis
- **API base URL:** `https://api.respan.ai`

## Authentication

### API Key

Use a Respan API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.respan.ai/docs/documentation/admin/keywords_api_keys)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /api/chat/completions` | [docs](https://www.respan.ai/docs/apis/gateway/create-chat-completion) |
| [Create Custom Model](actions/create-custom-model.md) | `POST /api/models/` | [docs](https://www.respan.ai/docs/apis/models/create-custom-model) |
| [Create Custom Provider](actions/create-custom-provider.md) | `POST /api/providers/` | [docs](https://www.respan.ai/docs/apis/models/create-custom-provider) |
| [Create Dataset](actions/create-dataset.md) | `POST /api/datasets/` | [docs](https://www.respan.ai/docs/apis/datasets/create-dataset) |
| [Create Prompt](actions/create-prompt.md) | `POST /api/prompts/` | [docs](https://www.respan.ai/docs/apis/prompts/create-prompt) |
| [Create Response](actions/create-response.md) | `POST /api/responses` | [docs](https://www.respan.ai/docs/apis/gateway/create-response) |
| [Create Testset](actions/create-testset.md) | `POST /api/testsets/` | [docs](https://www.respan.ai/docs/apis/testsets/create-testset) |
| [Get Prompts Summary](actions/get-prompts-summary.md) | `GET /api/prompts/summary/` | [docs](https://www.respan.ai/docs/apis/prompts/get-prompts-summary) |
| [Get Prompts Summary With Filters](actions/get-prompts-summary-with-filters.md) | `POST /api/prompts/summary/` | [docs](https://www.respan.ai/docs/apis/prompts/get-prompts-summary-with-filters) |
| [Health Check](actions/health-check.md) | `GET /health/` | [docs](https://www.respan.ai/docs/apis/health/check) |
| [List Custom Models](actions/list-custom-models.md) | `GET /api/models/` | [docs](https://www.respan.ai/docs/apis/models/list-custom-models) |
| [List Custom Providers](actions/list-custom-providers.md) | `GET /api/providers/` | [docs](https://www.respan.ai/docs/apis/models/list-custom-providers) |
| [List Datasets](actions/list-datasets.md) | `POST /api/datasets/list/` | [docs](https://www.respan.ai/docs/apis/datasets/list-datasets) |
| [List Models](actions/list-models.md) | `GET /api/models/public` | [docs](https://www.respan.ai/docs/apis/models/list-models) |
| [List Prompts](actions/list-prompts.md) | `GET /api/prompts/list/` | [docs](https://www.respan.ai/docs/apis/prompts/list-prompts) |
| [List Testsets](actions/list-testsets.md) | `POST /api/testsets/list/` | [docs](https://www.respan.ai/docs/apis/testsets/list-testsets) |
| [List Traces](actions/list-traces.md) | `POST /api/traces/list/` | [docs](https://www.respan.ai/docs/apis/traces/list-traces) |
