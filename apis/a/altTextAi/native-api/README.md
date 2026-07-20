# AltText.Ai: Native API Reference

A consolidated summary of AltText.Ai's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://alttext.ai/docs/
- **OpenAPI specification:** https://alttext.ai/openapi.yml
- **API base URL:** `https://alttext.ai/api/v1`

## Authentication

### API Key

Connect AltText.Ai using an API key from your AltText.ai account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://alttext.ai/docs/webui/account/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Upload Images](actions/bulk-upload-images.md) | `POST /images/bulk_create` | [docs](https://alttext.ai/apidocs#tag/Images/operation/bulk-create) |
| [Delete Image](actions/delete-image.md) | `DELETE /images/:asset_id` | [docs](https://alttext.ai/apidocs#tag/Images/operation/delete-image-by-asset-id) |
| [Generate Alt Text for Image](actions/generate-alt-text-for-image.md) | `POST /images` | [docs](https://alttext.ai/apidocs#tag/Images/operation/create-image) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://alttext.ai/apidocs#tag/Account/operation/get-account) |
| [Get Image](actions/get-image.md) | `GET /images/:asset_id` | [docs](https://alttext.ai/apidocs#tag/Images/operation/get-image-by-asset-id) |
| [List Images](actions/list-images.md) | `GET /images` | [docs](https://alttext.ai/apidocs#tag/Images/operation/get-images) |
| [Scrape Page Images](actions/scrape-page-images.md) | `POST /images/page_scrape` | [docs](https://alttext.ai/apidocs#tag/Images/operation/page-scrape) |
| [Search Images](actions/search-images.md) | `GET /images/search` | [docs](https://alttext.ai/apidocs#tag/Images/operation/search-images) |
| [Update Account](actions/update-account.md) | `PUT /account` | [docs](https://alttext.ai/apidocs#tag/Account/operation/update-account) |
| [Update Image](actions/update-image.md) | `PUT /images/:asset_id` | [docs](https://alttext.ai/apidocs#tag/Images/operation/update-image-by-asset-id) |
