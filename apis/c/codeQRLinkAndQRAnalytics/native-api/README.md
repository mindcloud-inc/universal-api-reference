# CodeQR - Link and QR Analytics: Native API Reference

A consolidated summary of CodeQR - Link and QR Analytics's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.codeqr.io/api-reference/introduction
- **OpenAPI specification:** https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml
- **API base URL:** `https://api.codeqr.io`

## Authentication

### API Key

Use a CodeQR project API key for internal integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.codeqr.io/api-reference/tokens)

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | `POST /domains` | [docs](https://docs.codeqr.io/api-reference/endpoint/create-a-domain) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Create QR Code](actions/create-qr-code.md) | `POST /qrcodes` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domains/:slug` | [docs](https://docs.codeqr.io/api-reference/endpoint/delete-a-domain) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/:linkId` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qrcodes/:qrcodeId` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:id` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Get Link](actions/get-link.md) | `GET /links/info` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectSlug` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qrcodes/info` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://docs.codeqr.io/api-reference/endpoint/retrieve-a-list-of-domains) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qrcodes` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Retrieve Analytics](actions/retrieve-analytics.md) | `GET /analytics` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Update Domain](actions/update-domain.md) | `PATCH /domains/:slug` | [docs](https://docs.codeqr.io/api-reference/endpoint/update-a-domain) |
| [Update Link](actions/update-link.md) | `PUT /links/:linkId` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /qrcodes/:qrcodeId` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:id` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Upsert Link](actions/upsert-link.md) | `PATCH /links/update` | [docs](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml) |
| [Upsert QR Code](actions/upsert-qr-code.md) | `PATCH /qrcodes/upsert` | [docs](https://docs.codeqr.io/api-reference/endpoint/upsert-a-qrcode) |
