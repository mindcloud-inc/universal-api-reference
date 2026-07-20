# Uniqode: Native API Reference

A consolidated summary of Uniqode's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.uniqode.com/
- **API base URL:** `https://api.uniqode.com/api/2.0`

## Authentication

### API Key

Authenticate with a Uniqode API key generated from the API section of the Uniqode dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.uniqode.com/en/articles/6064771-getting-started-with-static-and-dynamic-qr-code-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `page_size` in the query string to set the page size (default 50; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate QR Code](actions/activate-qr-code.md) | `PUT /qrcodes/:qrCodeId/activate/` | [docs](https://apidocs.uniqode.com/) |
| [Create Dynamic QR Code (Custom URL)](actions/create-dynamic-qr-code-custom-url.md) | `POST /qrcodes/` | [docs](https://apidocs.uniqode.com/) |
| [Create Landing Page](actions/create-landing-page.md) | `POST /markdowncards/` | [docs](https://apidocs.uniqode.com/) |
| [Create Media Object](actions/create-media-object.md) | `POST /media/` | [docs](https://apidocs.uniqode.com/) |
| [Create Static QR Code (Website)](actions/create-static-qr-code-website.md) | `POST /qrcodes/` | [docs](https://apidocs.uniqode.com/) |
| [Create Tag](actions/create-tag.md) | `POST /tags/` | [docs](https://apidocs.uniqode.com/) |
| [Deactivate QR Code](actions/deactivate-qr-code.md) | `DELETE /qrcodes/:qrCodeId/activate/` | [docs](https://apidocs.uniqode.com/) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /qrcodes/:qrCodeId/` | [docs](https://apidocs.uniqode.com/) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tagId/` | [docs](https://apidocs.uniqode.com/) |
| [Download QR Code Image](actions/download-qr-code-image.md) | `GET /qrcodes/:qrCodeId/download/` | [docs](https://apidocs.uniqode.com/) |
| [Get Landing Page](actions/get-landing-page.md) | `GET /markdowncards/:landingPageId/` | [docs](https://apidocs.uniqode.com/) |
| [Get Media Object](actions/get-media-object.md) | `GET /media/:mediaId/` | [docs](https://apidocs.uniqode.com/) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organizationId/` | [docs](https://apidocs.uniqode.com/) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qrcodes/:qrCodeId/` | [docs](https://apidocs.uniqode.com/) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tagId/` | [docs](https://apidocs.uniqode.com/) |
| [List Landing Pages](actions/list-landing-pages.md) | `GET /markdowncards/` | [docs](https://apidocs.uniqode.com/) |
| [List Media Objects](actions/list-media-objects.md) | `GET /media/` | [docs](https://apidocs.uniqode.com/) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations/` | [docs](https://apidocs.uniqode.com/) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qrcodes/` | [docs](https://apidocs.uniqode.com/) |
| [List Tags](actions/list-tags.md) | `GET /tags/` | [docs](https://apidocs.uniqode.com/) |
| [Update Landing Page](actions/update-landing-page.md) | `PUT /markdowncards/:landingPageId/` | [docs](https://apidocs.uniqode.com/) |
| [Update Media Object](actions/update-media-object.md) | `PUT /media/:mediaId/` | [docs](https://apidocs.uniqode.com/) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /qrcodes/:qrCodeId/` | [docs](https://apidocs.uniqode.com/) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:tagId/` | [docs](https://apidocs.uniqode.com/) |
