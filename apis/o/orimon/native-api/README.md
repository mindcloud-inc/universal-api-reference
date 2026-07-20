# Orimon: Native API Reference

A consolidated summary of Orimon's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://orimon.gitbook.io/docs/developer-api/getting-started-with-apis
- **API base URL:** `https://channel-connector.orimon.ai`

## Authentication

### API Key

Connect using your Orimon API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://orimon.gitbook.io/docs/developer-api/getting-started-with-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | `POST /orimon/v1/conversation/api/message` | [docs](https://orimon.gitbook.io/docs/developer-api/message-api) |
