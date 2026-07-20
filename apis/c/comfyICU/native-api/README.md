# Comfy.ICU: Native API Reference

A consolidated summary of Comfy.ICU's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://comfy.icu/docs/api
- **API base URL:** `https://comfy.icu`

## Authentication

### API Key

Authenticate Comfy.ICU requests with an API key in the Authorization bearer token header.

### Credentials

- **Comfy.ICU API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://comfy.icu/docs/api)

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
| [Get Run Status](actions/get-run-status.md) | `GET /api/v1/workflows/:workflow_id/runs/:run_id` | [docs](https://comfy.icu/docs/api) |
| [Run Workflow](actions/run-workflow.md) | `POST /api/v1/workflows/:workflow_id/runs` | [docs](https://comfy.icu/docs/api) |
