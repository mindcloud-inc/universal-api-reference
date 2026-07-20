# Memix: Native API Reference

A consolidated summary of Memix's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://api.memix.com/docs
- **OpenAPI specification:** https://api.memix.com/openapi.json
- **API base URL:** `https://api.memix.com`

## Authentication

### No Auth

No authentication required for the documented public Memix API.

This API does not require request authentication.

[Official authentication documentation](https://api.memix.com/docs)

## API conventions

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate GIF Memix](actions/generate-gif-memix.md) | `GET /memix-:template_slug.gif` |  |
| [Generate JPEG Memix](actions/generate-jpeg-memix.md) | `GET /memix-:template_slug.jpeg` |  |
| [Generate MP4 Memix](actions/generate-mp4-memix.md) | `GET /memix-:template_slug.mp4` |  |
| [Generate WebP Memix](actions/generate-web-p-memix.md) | `GET /memix-:template_slug.webp` |  |
| [Get All Templates](actions/get-all-templates.md) | `GET /v1/templates/all` | [docs](https://api.memix.com/docs) |
| [Get Referrals Status](actions/get-referrals-status.md) | `GET /v1/referrals-status` |  |
| [Get Subscription Status](actions/get-subscription-status.md) | `GET /v1/subscriptions` |  |
| [Get Template Details](actions/get-template-details.md) | `GET /v1/templates/:template_slug` |  |
| [Get Template Shortcuts](actions/get-template-shortcuts.md) | `GET /v1/templates/search/shortcuts` |  |
| [Preview GIF Memix](actions/preview-gif-memix.md) | `GET /preview/memix-:template_slug.gif` |  |
| [Preview JPEG Memix](actions/preview-jpeg-memix.md) | `GET /preview/memix-:template_slug.jpeg` |  |
| [Preview MP4 Memix](actions/preview-mp4-memix.md) | `GET /preview/memix-:template_slug.mp4` |  |
| [Preview WebP Memix](actions/preview-web-p-memix.md) | `GET /preview/memix-:template_slug.webp` |  |
| [Search Curated Templates](actions/search-curated-templates.md) | `GET /v1/templates/search` |  |
| [Search Templates By Image URL](actions/search-templates-by-image-url.md) | `GET /v1/templates/search` |  |
| [Search Templates By Query](actions/search-templates-by-query.md) | `GET /v1/templates/search` |  |
| [Search Templates By Text](actions/search-templates-by-text.md) | `GET /v1/templates/search` |  |
