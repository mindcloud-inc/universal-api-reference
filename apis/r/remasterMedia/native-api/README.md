# RemasterMedia: Native API Reference

A consolidated summary of RemasterMedia's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.remastermedia.com/developers
- **API base URL:** `https://api-sandbox.remastermedia.com/v2`

## Authentication

### Client credentials

Authenticate to RemasterMedia by exchanging a client ID and client key for a JWT token via POST /auth.

### Credentials

- **Client ID:** `clientId` · required · RemasterMedia API client ID.
- **Client Key:** `clientKey` · required · RemasterMedia API client key.

Send these headers with each API request:

```http
Authorization: <custom.token>
```

[Official authentication documentation](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /auth` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#authentication-and-authorization-authentication-post) |
| [Create Mediafile](actions/create-mediafile.md) | `POST /mediafiles/create` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-create-new-mediafile-post) |
| [Create Poster](actions/create-poster.md) | `POST /mediafiles/process` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-2) |
| [Create Remaster](actions/create-remaster.md) | `POST /mediafiles/process` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post) |
| [Create Waveform](actions/create-waveform.md) | `POST /mediafiles/process` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-1) |
| [Denoise Mediafile](actions/denoise-mediafile.md) | `POST /mediafiles/process` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-3) |
| [Denoise Mediafile With Parameters](actions/denoise-mediafile-with-parameters.md) | `POST /mediafiles/process` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile-post-3) |
| [Get Mediafile](actions/get-mediafile.md) | `GET /mediafiles/{{id}}` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-mediafile-details-get) |
| [Get Source Mediafile](actions/get-source-mediafile.md) | `GET /mediafile/{{id}}/source` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-source-mediafile-get) |
| [List Denoise Presets](actions/list-denoise-presets.md) | `GET /actions/denoise/presets` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#action-details-list-noise-reduction-presets-get) |
| [List Derived Mediafiles](actions/list-derived-mediafiles.md) | `GET /mediafile/{{id}}/derived` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-derived-mediafiles-get) |
| [List Mediafiles](actions/list-mediafiles.md) | `GET /mediafiles` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-mediafiles-collection-get) |
| [List Remastering Presets](actions/list-remastering-presets.md) | `GET /actions/remaster/presets` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#action-details-list-remastering-presets-get) |
| [Process Mediafile](actions/process-mediafile.md) | `POST /mediafiles/process` | [docs](https://remastermedia-web-assets.s3-accelerate.amazonaws.com/api_reference-v2.html#mediafiles-process-mediafile) |
