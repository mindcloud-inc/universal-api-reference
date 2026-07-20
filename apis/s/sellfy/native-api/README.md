# Sellfy: Native API Reference

A consolidated summary of Sellfy's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.sellfy.com/article/348-oembed
- **API base URL:** `https://sellfy.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.sellfy.com/article/124-zapier)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get oEmbed](actions/get-oembed.md) | `GET /oembed/` | [docs](https://docs.sellfy.com/article/348-oembed) |
