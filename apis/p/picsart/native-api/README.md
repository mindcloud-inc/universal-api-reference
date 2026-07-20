# Picsart: Native API Reference

A consolidated summary of Picsart's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.picsart.io/reference
- **API base URL:** `https://api.picsart.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.picsart.io/docs/creative-apis-keys-secrets)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429`. Wait 5000 ms before the first retry. Stop after 1 attempts.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Adjust Image](actions/adjust-image.md) | `POST /tools/1.0/adjust` | [docs](https://docs.picsart.io/reference/image-adjust) |
| [Blend Images](actions/blend-images.md) | `POST /tools/1.0/blend` | [docs](https://docs.picsart.io/reference/image-blend) |
| [Edit Image](actions/edit-image.md) | `POST /tools/1.0/edit` | [docs](https://docs.picsart.io/reference/image-edit) |
| [Get AI Effect Names](actions/get-ai-effect-names.md) | `GET /tools/1.0/effects/ai` | [docs](https://docs.picsart.io/reference/image-list-ai-effect-names) |
| [Get Credits Balance](actions/get-credits-balance.md) | `GET /tools/1.0/balance` | [docs](https://docs.picsart.io/reference/image-credits-balance) |
| [Get Effect Names](actions/get-effect-names.md) | `GET /tools/1.0/effects` | [docs](https://docs.picsart.io/reference/image-list-effect-names) |
| [Remove Background](actions/remove-background.md) | `POST /tools/1.0/removebg` | [docs](https://docs.picsart.io/reference/image-remove-background) |
| [Transfer Image Colors](actions/transfer-image-colors.md) | `POST /tools/1.0/color-transfer` | [docs](https://docs.picsart.io/reference/image-transfer-color) |
| [Transfer Image Style](actions/transfer-image-style.md) | `POST /tools/1.0/styletransfer` | [docs](https://docs.picsart.io/reference/image-transfer-style) |
| [Upscale Image](actions/upscale-image.md) | `POST /tools/1.0/upscale` | [docs](https://docs.picsart.io/reference/image-upscale) |
| [Vectorize Image](actions/vectorize-image.md) | `POST /tools/1.0/vectorizer` | [docs](https://docs.picsart.io/reference/image-vectorize-raster-to-svg) |
