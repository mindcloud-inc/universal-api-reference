# easybits Extractor: Native API Reference

A consolidated summary of easybits Extractor's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://extractor.easybits.tech/documentation/integration
- **API base URL:** `https://extractor.easybits.tech/api`

## Authentication

### Pipeline API Key

Use the API key and pipeline ID from your easybits Extractor pipeline details page.

### Credentials

- **API Key:** `apiKey` · required
- **Pipeline ID:** `pipelineId` · required · Pipeline ID from the easybits Extractor pipeline details page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://extractor.easybits.tech/documentation/integration)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract Data](actions/extract-data.md) | `POST /pipelines/:pipelineId` | [docs](https://extractor.easybits.tech/documentation/integration) |
| [Verify Pipeline Connection](actions/verify-pipeline-connection.md) | `GET /pipelines/:pipelineId/test` | [docs](https://extractor.easybits.tech/documentation/integration) |
