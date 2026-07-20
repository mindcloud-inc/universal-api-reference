# CaptureIQ: Native API Reference

A consolidated summary of CaptureIQ's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://help.captureiq.ai/api-reference/getting-started
- **OpenAPI specification:** https://help.captureiq.ai/api-reference/openapi.json
- **API base URL:** `https://www.app.captureiq.ai`

## Authentication

### API Key

Use a CaptureIQ API key from Account Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.captureiq.ai/api-reference/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Retrieve Recent Form Submission](actions/retrieve-recent-form-submission.md) | `GET /ciq/recent-submission/v1` | [docs](https://help.captureiq.ai/api-reference/recent-submissions) |
| [Validate API Key](actions/validate-api-key.md) | `GET /api/validateApiKey` | [docs](https://help.captureiq.ai/api-reference/validate-api-key) |
