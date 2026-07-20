# Tinify: Native API Reference

A consolidated summary of Tinify's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://tinify.com/developers/reference/http
- **API base URL:** `https://api.tinify.com`

## Authentication

### HTTP Basic

Authenticate to Tinify with HTTP Basic Auth using username `api` and the Tinify API key as the password.

### Credentials

- **Username:** `username` · required
- **API key:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://tinify.com/developers/reference/http#authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compress Image From File](actions/compress-image-from-file.md) | `POST /shrink` | [docs](https://tinify.com/developers/reference/http#compressing-images) |
| [Compress Image From URL](actions/compress-image-from-url.md) | `POST /shrink` | [docs](https://tinify.com/developers/reference/http#compressing-images) |
| [Convert Image](actions/convert-image.md) | `POST /output/:outputId` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Convert Image With Background](actions/convert-image-with-background.md) | `POST /output/:outputId` | [docs](https://tinify.com/developers/reference/http#converting-images) |
| [Download Optimized Image](actions/download-optimized-image.md) | `GET /output/:outputId` | [docs](https://tinify.com/developers/reference/http#compressing-images) |
| [Preserve Metadata](actions/preserve-metadata.md) | `POST /output/:outputId` | [docs](https://tinify.com/developers/reference/http#preserving-metadata) |
| [Resize Image](actions/resize-image.md) | `POST /output/:outputId` | [docs](https://tinify.com/developers/reference/http#resizing-images) |
| [Store Image To Amazon S3](actions/store-image-to-amazon-s3.md) | `POST /output/:outputId` | [docs](https://tinify.com/developers/reference/http#saving-to-amazon-s3) |
| [Store Image To Google Cloud Storage](actions/store-image-to-google-cloud-storage.md) | `POST /output/:outputId` | [docs](https://tinify.com/developers/reference/http#saving-to-google-cloud-storage) |
