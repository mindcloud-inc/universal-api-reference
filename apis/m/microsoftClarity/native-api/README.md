# Microsoft Clarity: Native API Reference

A consolidated summary of Microsoft Clarity's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/clarity/setup-and-installation/clarity-data-export-api
- **API base URL:** `https://www.clarity.ms`

## Authentication

### API Key

Connect Microsoft Clarity with a Data Export API token from your Clarity project settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/clarity/setup-and-installation/clarity-data-export-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Project Live Insights](actions/get-project-live-insights.md) | `GET /export-data/api/v1/project-live-insights` | [docs](https://learn.microsoft.com/en-us/clarity/setup-and-installation/clarity-data-export-api) |
