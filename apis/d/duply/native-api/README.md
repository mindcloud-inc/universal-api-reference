# Duply: Native API Reference

A consolidated summary of Duply's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://app.duply.co/docs
- **API base URL:** `https://gen.duply.co/v1`

## Authentication

### Basic Auth

Use your Duply API key as the username and your secret key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://app.duply.co/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | `POST /generate/` | [docs](https://app.duply.co/docs#post-generate-image) |
| [Generate Video](actions/generate-video.md) | `POST /generate-video/` | [docs](https://app.duply.co/docs#post-generate-video) |
| [Get Generated Image Detail](actions/get-generated-image-detail.md) | `GET /generate/:generateId` | [docs](https://app.duply.co/docs#get-generate-api-detail) |
| [Get Generated Video Detail](actions/get-generated-video-detail.md) | `GET /generate-video/:generateId` | [docs](https://app.duply.co/docs#get-generate-api-video-detail) |
| [Get Template Detail](actions/get-template-detail.md) | `GET /template/:templateId` | [docs](https://app.duply.co/docs#get-template-detail) |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://app.duply.co/docs#get-usage) |
| [List Generated Images](actions/list-generated-images.md) | `GET /generate/` | [docs](https://app.duply.co/docs#get-generate-api-list) |
| [List Generated Videos](actions/list-generated-videos.md) | `GET /generate-video/` | [docs](https://app.duply.co/docs#get-generate-api-video-list) |
| [List My Templates](actions/list-my-templates.md) | `GET /template` | [docs](https://app.duply.co/docs#get-list-template) |
| [Test Authentication](actions/test-authentication.md) | `GET /auth` | [docs](https://app.duply.co/docs#authentication) |
