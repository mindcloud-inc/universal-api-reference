# LogSnag: Native API Reference

A consolidated summary of LogSnag's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.logsnag.com
- **API base URL:** `https://api.logsnag.com/v1`

## Authentication

### API Key

Use a LogSnag personal API token. MindCloud sends it as Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.logsnag.com/api-reference/log)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Group User](actions/group-user.md) | `POST /group` | [docs](https://docs.logsnag.com/sdks/node) |
| [Identify User](actions/identify-user.md) | `POST /identify` | [docs](https://docs.logsnag.com/api-reference/identify) |
| [Mutate Insight](actions/mutate-insight.md) | `PATCH /insight` | [docs](https://docs.logsnag.com/api-reference/insight-mutate) |
| [Publish Insight](actions/publish-insight.md) | `POST /insight` | [docs](https://docs.logsnag.com/api-reference/insight) |
| [Publish Log Event](actions/publish-log-event.md) | `POST /log` | [docs](https://docs.logsnag.com/api-reference/log) |
| [Track Page View](actions/track-page-view.md) | `POST /page` | [docs](https://docs.logsnag.com/sdks/node) |
