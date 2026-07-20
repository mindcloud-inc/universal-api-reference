# NASA Image and Video Library: Native API Reference

A consolidated summary of NASA Image and Video Library's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf
- **API base URL:** `https://images-api.nasa.gov`

## Authentication

### No Authentication

Public NASA API with no authentication required.

This API does not require request authentication.

[Official authentication documentation](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Album Contents](actions/get-album-contents.md) | `GET /album/:album_name` | [docs](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf) |
| [Get Asset Manifest](actions/get-asset-manifest.md) | `GET /asset/:nasa_id` | [docs](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf) |
| [Get Asset Metadata Location](actions/get-asset-metadata-location.md) | `GET /metadata/:nasa_id` | [docs](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf) |
| [Get Video Captions Location](actions/get-video-captions-location.md) | `GET /captions/:nasa_id` | [docs](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf) |
| [Search Assets](actions/search-assets.md) | `GET /search` | [docs](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf) |
