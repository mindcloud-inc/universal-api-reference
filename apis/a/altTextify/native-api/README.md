# AltTextify: Native API Reference

A consolidated summary of AltTextify's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.alttextify.net/
- **API base URL:** `https://api.alttextify.net/api/v1`

## Authentication

### API Key

Use an AltTextify API key passed in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://apidoc.alttextify.net/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud/1.0` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Image](actions/delete-image.md) | `DELETE /image/:asset_id` | [docs](https://apidoc.alttextify.net/#api-Image-DeleteImage) |
| [Get Image](actions/get-image.md) | `GET /image/:asset_id` | [docs](https://apidoc.alttextify.net/#api-Image-GetImageByAssetID) |
| [List Images](actions/list-images.md) | `GET /image` | [docs](https://apidoc.alttextify.net/#api-Image-GetImages) |
| [Upload Image From URL](actions/upload-image-from-url.md) | `POST /image/url` | [docs](https://apidoc.alttextify.net/#api-Image-UploadImageURL) |
| [Upload Raw Image](actions/upload-raw-image.md) | `POST /image/raw` | [docs](https://apidoc.alttextify.net/#api-Image-UploadRawImage) |
