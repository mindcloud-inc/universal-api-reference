# PrexView: Native API Reference

A consolidated summary of PrexView's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://prexview.com/docs/api/
- **API base URL:** `https://api.prexview.com`

## Authentication

### API Key

Authenticate requests with a PrexView API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://prexview.com/docs/api/)

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create document from JSON](actions/create-document-from-json.md) | `POST /v1/transform` | [docs](https://prexview.com/docs/api/) |
| [Create document from XML](actions/create-document-from-xml.md) | `POST /v1/transform` | [docs](https://prexview.com/docs/api/) |
