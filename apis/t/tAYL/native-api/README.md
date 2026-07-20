# TAYL: Native API Reference

A consolidated summary of TAYL's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://my.tayl.app/create/api
- **API base URL:** `https://x.tayl.app`

## Authentication

### API Key

Use a TAYL tenant API key. TAYL requires the credential in the x-api-key header, not as bearer auth.

### Credentials

- **API Key:** `apiKey` · required · TAYL tenant API key used in the x-api-key request header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://my.tayl.app/create/api)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Tale From Text](actions/create-tale-from-text.md) | `POST /submit` | [docs](https://my.tayl.app/create/api) |
| [Create Tale From URL](actions/create-tale-from-url.md) | `POST /submit` | [docs](https://my.tayl.app/create/api) |
| [List Tales](actions/list-tales.md) | `GET /tales` | [docs](https://my.tayl.app/create/api) |
