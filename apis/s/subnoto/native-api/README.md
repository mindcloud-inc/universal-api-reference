# Subnoto: Native API Reference

A consolidated summary of Subnoto's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://subnoto.com/documentation
- **API base URL:** `https://app.subnoto.com`

## Authentication

### API Key

Authenticate through a deployed Subnoto API proxy by pasting one combined value in the API Key field: accessKey:secretKey.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://subnoto.com/documentation/developers/encryption-proxy)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | `POST /public/workspace/list` | [docs](https://subnoto.com/documentation/developers/openapi/operations/publicworkspacelist) |
| [Who Am I](actions/who-am-i.md) | `POST /public/utils/whoami` | [docs](https://subnoto.com/documentation/developers/openapi/operations/publicutilswhoami) |
