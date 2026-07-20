# Calculate Video Transcription Price with deAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/transcribe/price-calculation`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_ts` | body | `string` | no | Whether the transcription should include timestamps. |
| `model` | body | `string` | no | Transcription model slug from List Models. |
| `source_url` | body | `string` | no | Audio or video URL to price for transcription. |
