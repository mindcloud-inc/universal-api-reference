# PIMMS: Native API Reference

A consolidated summary of PIMMS's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://pimms.apidocumentation.com/reference
- **API base URL:** `https://api.pimms.io`

## Authentication

### API Key

Use your PIMMS workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pimms.apidocumentation.com/reference)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://pimms.apidocumentation.com/reference#tag/links/POST/links) |
| [Create Referrals Embed Token](actions/create-referrals-embed-token.md) | `POST /tokens/embed/referrals` | [docs](https://pimms.apidocumentation.com/reference#tag/embed-tokens/POST/tokens/embed/referrals) |
| [Retrieve Analytics](actions/retrieve-analytics.md) | `GET /analytics` | [docs](https://pimms.apidocumentation.com/reference#tag/analytics/GET/analytics) |
| [Retrieve QR Code](actions/retrieve-qr-code.md) | `GET /qr` | [docs](https://pimms.apidocumentation.com/reference#tag/qr-codes/GET/qr) |
| [Track Lead](actions/track-lead.md) | `POST /track/lead` | [docs](https://pimms.apidocumentation.com/reference#tag/track/POST/track/lead) |
| [Track Sale](actions/track-sale.md) | `POST /track/sale` | [docs](https://pimms.apidocumentation.com/reference#tag/track/POST/track/sale) |
| [Upsert Link](actions/upsert-link.md) | `PUT /links/upsert` | [docs](https://pimms.apidocumentation.com/reference#tag/links/PUT/links/upsert) |
