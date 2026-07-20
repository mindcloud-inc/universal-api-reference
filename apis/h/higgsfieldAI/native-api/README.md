# Higgsfield AI: Native API Reference

A consolidated summary of Higgsfield AI's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.higgsfield.ai/how-to/introduction
- **API base URL:** `https://platform.higgsfield.ai`

## Authentication

### API Key

Connect with a Higgsfield API key and secret combined as API key:API secret.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.higgsfield.ai/how-to/sdk)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 0.2 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Pending Request](actions/cancel-pending-request.md) | `POST /requests/{requestId}/cancel` | [docs](https://docs.higgsfield.ai/how-to/introduction) |
| [Generate File Upload URL](actions/generate-file-upload-url.md) | `POST /files/generate-upload-url` | [docs](https://docs.higgsfield.ai/how-to/sdk) |
| [Generate Image with Seedream v4](actions/generate-image-with-seedream-v4.md) | `POST /bytedance/seedream/v4/text-to-image` | [docs](https://docs.higgsfield.ai/how-to/sdk) |
| [Generate Image with Soul Standard](actions/generate-image-with-soul-standard.md) | `POST /higgsfield-ai/soul/standard` | [docs](https://docs.higgsfield.ai/guides/images) |
| [Generate Video with DoP Standard](actions/generate-video-with-dop-standard.md) | `POST /higgsfield-ai/dop/standard` | [docs](https://docs.higgsfield.ai/guides/video) |
| [Generate Video with Kling 2.1 Pro](actions/generate-video-with-kling21-pro.md) | `POST /kling-video/v2.1/pro/image-to-video` | [docs](https://docs.higgsfield.ai/guides/video) |
| [Generate Video with Seedance 1.0 Pro](actions/generate-video-with-seedance10-pro.md) | `POST /bytedance/seedance/v1/pro/image-to-video` | [docs](https://docs.higgsfield.ai/guides/video) |
| [Get Request Status](actions/get-request-status.md) | `GET /requests/{requestId}/status` | [docs](https://docs.higgsfield.ai/how-to/introduction) |
| [Submit Generation Request](actions/submit-generation-request.md) | `POST /{modelId}` | [docs](https://docs.higgsfield.ai/how-to/introduction) |
