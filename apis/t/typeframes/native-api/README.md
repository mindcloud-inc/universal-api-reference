# Typeframes: Native API Reference

A consolidated summary of Typeframes's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/36975521/2sBXcGEfaB
- **OpenAPI specification:** https://www.revid.ai/postman/revid-public-v3-render.openapi.json
- **API base URL:** `https://www.revid.ai/api/public`

## Authentication

### API Key

Use your Revid API key. Revid public API requests send the key in the `key` header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
key: <apiKey>
```

[Official authentication documentation](https://www.revid.ai/api/public/v3/render)

## API conventions

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Projects](actions/get-projects.md) | `GET /v2/projects` | [docs](https://www.revid.ai/api/public/v3/render) |
