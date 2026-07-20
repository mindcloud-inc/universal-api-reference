# deAPI: Native API Reference

A consolidated summary of deAPI's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.deapi.ai/api/overview
- **API base URL:** `https://api.deapi.ai`

## Authentication

### API Key

Use your deAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.deapi.ai/quickstart)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Image Prompt Price](actions/calculate-image-prompt-price.md) | `POST /api/v1/client/prompt/image/price-calculation` |  |
| [Calculate Text-to-Embedding Price](actions/calculate-text-to-embedding-price.md) | `POST /api/v1/client/txt2embedding/price-calculation` |  |
| [Calculate Text-to-Image Price](actions/calculate-text-to-image-price.md) | `POST /api/v1/client/txt2img/price-calculation` |  |
| [Calculate Text-to-Music Price](actions/calculate-text-to-music-price.md) | `POST /api/v1/client/txt2music/price-calculation` |  |
| [Calculate Text-to-Speech Price](actions/calculate-text-to-speech-price.md) | `POST /api/v1/client/txt2audio/price-calculation` |  |
| [Calculate Text-to-Video Price](actions/calculate-text-to-video-price.md) | `POST /api/v1/client/txt2video/price-calculation` |  |
| [Calculate Video Transcription Price](actions/calculate-transcription-price.md) | `POST /api/v1/client/transcribe/price-calculation` |  |
| [Create Text-to-Embedding Job](actions/create-text-to-embedding-job.md) | `POST /api/v1/client/txt2embedding` |  |
| [Create Text-to-Image Job](actions/create-text-to-image-job.md) | `POST /api/v1/client/txt2img` |  |
| [Create Text-to-Music Job](actions/create-text-to-music-job.md) | `POST /api/v1/client/txt2music` |  |
| [Create Text-to-Speech Job](actions/create-text-to-speech-job.md) | `POST /api/v1/client/txt2audio` |  |
| [Create Text-to-Video Job](actions/create-text-to-video-job.md) | `POST /api/v1/client/txt2video` |  |
| [Create Video Transcription Job](actions/create-transcription-job.md) | `POST /api/v1/client/transcribe` |  |
| [Enhance Image Prompt](actions/enhance-image-prompt.md) | `POST /api/v1/client/prompt/image` |  |
| [Enhance Speech Prompt](actions/enhance-speech-prompt.md) | `POST /api/v1/client/prompt/speech` |  |
| [Get Current Balance](actions/get-current-balance.md) | `GET /api/v1/client/balance` | [docs](https://docs.deapi.ai/api/utilities/check-balance) |
| [Get Request Status](actions/get-request-status.md) | `GET /api/v1/client/request-status/:request_id` |  |
| [Get Sample Prompts](actions/get-sample-prompts.md) | `GET /api/v1/client/prompts/samples` |  |
| [List Models](actions/list-models.md) | `GET /api/v1/client/models` |  |
