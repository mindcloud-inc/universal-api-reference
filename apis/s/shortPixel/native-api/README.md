# ShortPixel: Native API Reference

A consolidated summary of ShortPixel's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://shortpixel.com/api-docs
- **API base URL:** `https://api.shortpixel.com`

## Authentication

### API Key

Authenticate ShortPixel requests with the tenant API key sent as request field key.

### Credentials

- **API Key:** `apiKey` · required · Your ShortPixel tenant API key.

[Official authentication documentation](https://shortpixel.com/api-docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Remote Optimization Status](actions/check-remote-optimization-status.md) | `POST /v2/reducer.php` | [docs](https://shortpixel.com/api-docs) |
| [Check Uploaded Optimization Status](actions/check-uploaded-optimization-status.md) | `POST /v2/post-reducer.php` | [docs](https://shortpixel.com/api-docs) |
| [Optimize Remote Image Direct](actions/optimize-remote-image-direct.md) | `POST /v2/reducer-sync.php` | [docs](https://shortpixel.com/api-docs) |
| [Optimize Remote Images](actions/optimize-remote-images.md) | `POST /v2/reducer.php` | [docs](https://shortpixel.com/api-docs) |
| [Optimize Uploaded Images](actions/optimize-uploaded-images.md) | `POST /v2/post-reducer.php` | [docs](https://shortpixel.com/api-docs) |
