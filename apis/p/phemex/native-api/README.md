# Phemex: Native API Reference

A consolidated summary of Phemex's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://phemex-docs.github.io/
- **API base URL:** `https://api.phemex.com`

## Authentication

### API Key

Use a Phemex API key and API secret to sign private REST requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://phemex.com/help-center/how-do-i-create-an-api-key)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Products](actions/list-products.md) | `GET /public/products` | [docs](https://phemex-docs.github.io/#query-product-information) |
| [List Spot Assets](actions/list-spot-assets.md) | `GET /spot/wallets` | [docs](https://phemex-docs.github.io/#query-wallets) |
