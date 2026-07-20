# Gyazo: Native API Reference

A consolidated summary of Gyazo's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://gyazo.com/api/docs/user
- **API base URL:** `https://api.gyazo.com`

## Authentication

### OAuth 2.0

Connect a Gyazo user account with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://gyazo.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://gyazo.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public`.

[Official authentication documentation](https://gyazo.com/api/docs/auth)

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Image](actions/delete-image.md) | `DELETE /api/images/:image_id` | [docs](https://gyazo.com/api/docs/image) |
| [Get Current User](actions/get-current-user.md) | `GET /api/users/me` | [docs](https://gyazo.com/api/docs/user) |
| [Get Image](actions/get-image.md) | `GET /api/images/:image_id` | [docs](https://gyazo.com/api/docs/image) |
| [Get Image OEmbed](actions/get-image-o-embed.md) | `GET /api/oembed` | [docs](https://gyazo.com/api/docs/image) |
| [List Images](actions/list-images.md) | `GET /api/images` | [docs](https://gyazo.com/api/docs/image) |
| [Search Images](actions/search-images.md) | `GET /api/search` | [docs](https://gyazo.com/api/docs/search) |
| [Upload Image](actions/upload-image.md) | `POST https://upload.gyazo.com/api/upload` | [docs](https://gyazo.com/api/docs/image) |
