# change.photos: Native API Reference

A consolidated summary of change.photos's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.change.photos/api-docs
- **API base URL:** `https://www.change.photos`

## Authentication

### API Key

Use a change.photos API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.change.photos/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Adjust Image Quality](actions/adjust-image-quality.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Blur Image](actions/blur-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Compress Image](actions/compress-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Convert Image Format](actions/convert-image-format.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Flip Image Horizontally](actions/flip-image-horizontally.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Flip Image Vertically](actions/flip-image-vertically.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Grayscale Image](actions/grayscale-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Resize Image](actions/resize-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Rotate Image](actions/rotate-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Sharpen Image](actions/sharpen-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Tint Image](actions/tint-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
| [Transform Image](actions/transform-image.md) | `POST /api/change` | [docs](https://www.change.photos/api-docs) |
