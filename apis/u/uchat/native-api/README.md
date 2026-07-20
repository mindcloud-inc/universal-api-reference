# Uchat: Native API Reference

A consolidated summary of Uchat's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://uchat.io/doc/2/API
- **API base URL:** `https://api.uchat.io`

## Authentication

### API Token

Authenticate with a Uchat room API token.

### Credentials

- **API Key:** `apiKey` · required
- **Room:** `room` · required · Uchat room identifier used in the X-UCHAT-API-ROOM request header.

Send these headers with each API request:

```http
X-UCHAT-API-ROOM: <room>
X-UCHAT-API-TOKEN: <apiKey>
```

[Official authentication documentation](https://uchat.io/doc/2.5/%EC%84%9C%EB%B2%84-API)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `uchat_api_client_v1` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Plugin Message](actions/send-plugin-message.md) | `POST /plugin/:pluginId` | [docs](https://uchat.io/doc/2.5/%EC%84%9C%EB%B2%84-API) |
