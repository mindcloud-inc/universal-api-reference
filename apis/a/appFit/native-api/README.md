# AppFit: Native API Reference

A consolidated summary of AppFit's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.appfit.io/documentation/overview
- **API base URL:** `https://api.appfit.io`

## Authentication

### API Key

Use an AppFit API key to send events to AppFit.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.appfit.io/article/website-integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Track Metric Event](actions/track-metric-event.md) | `POST /metric-events` | [docs](https://www.appfit.io/article/website-integration) |
| [Track Metric Event Batch](actions/track-metric-event-batch.md) | `POST /metric-events/batch` | [docs](https://www.appfit.io/article/website-integration) |
