# Imejis.io: Native API Reference

A consolidated summary of Imejis.io's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.imejis.io/apis
- **API base URL:** `https://render.imejis.io/v1`

## Authentication

### API Key

Authenticate requests with the Imejis.io API key sent in the dma-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
dma-api-key: <apiKey>
```

[Official authentication documentation](https://www.imejis.io/apis/javascript)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Render Image](actions/render-image.md) | `POST :design_id` | [docs](https://www.imejis.io/apis/curl) |
