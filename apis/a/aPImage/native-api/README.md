# APImage: Native API Reference

A consolidated summary of APImage's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://apimage.org/docs/api-reference
- **API base URL:** `https://apimage.org/api`

## Authentication

### APImage API Key

Bearer API key authentication for the APImage Image Studio API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.apimage.org/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Image](actions/analyze-image.md) | `POST /ai-image-to-text` | [docs](https://support.apimage.org/article/18-how-to-use-the-ai-image-analyzer) |
| [Enhance Prompt](actions/enhance-prompt.md) | `POST https://app.apimage.org/api/v1/image-studio` | [docs](https://apimage.org/docs/api-reference#enhance-prompt) |
| [Generate Image](actions/generate-image.md) | `POST https://app.apimage.org/api/v1/image-studio` | [docs](https://apimage.org/docs/api-reference#generate) |
| [Remove Background](actions/remove-background.md) | `POST https://app.apimage.org/api/v1/image-studio` | [docs](https://apimage.org/docs/api-reference#background-removal) |
