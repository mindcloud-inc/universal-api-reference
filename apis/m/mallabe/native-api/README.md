# Mallabe: Native API Reference

A consolidated summary of Mallabe's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://rapidapi.com/mallabe1/api/mallabe
- **API base URL:** `https://mallabe.p.rapidapi.com/v1`

## Authentication

### API Key

Connect with your RapidAPI key for Mallabe.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-RapidAPI-Key: <apiKey>
```

[Official authentication documentation](https://docs.rapidapi.com/docs/keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compress Image](actions/compress-image.md) | `POST /images/compress` | [docs](https://rapidapi.com/mallabe1/api/mallabe) |
| [Convert Currency](actions/convert-currency.md) | `POST /currencies/convert` | [docs](https://app.mallabe.com/currencies/convert/) |
| [Get Image Metadata](actions/get-image-metadata.md) | `POST /images/metadata` | [docs](https://rapidapi.com/mallabe1/api/mallabe) |
| [Get Website Status](actions/get-website-status.md) | `POST /websites/status` | [docs](https://app.mallabe.com/websites/status/) |
| [Get Website Thumbnail](actions/get-website-thumbnail.md) | `POST /websites/thumbnail` | [docs](https://app.mallabe.com/websites/thumbnail/) |
| [Parse User Agent](actions/parse-user-agent.md) | `POST /uas/parse` | [docs](https://app.mallabe.com/user-agents/parse/) |
| [Resize Image](actions/resize-image.md) | `POST /images/resize` | [docs](https://app.mallabe.com/images/resize/) |
| [Upload File](actions/upload-file.md) | `POST /files/upload` | [docs](https://rapidapi.com/mallabe1/api/mallabe) |
