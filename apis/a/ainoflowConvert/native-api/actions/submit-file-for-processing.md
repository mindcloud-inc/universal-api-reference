# Submit File for Processing with Ainoflow Convert

Creates a conversion job in Ainoflow Convert from an uploaded file.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/convert/submit-file`
- **Base URL:** `https://api.ainoflow.io`
- **Official documentation:** [Submit File for Processing](https://www.ainoflow.io/docs/api/convert)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document or audio file to process. |
| `languages` | body | `string` | yes | Comma-separated language codes. Send multiple values as a string separated by `,`. |
| `outputs` | body | `string` | yes | Comma-separated output formats. Send multiple values as a string separated by `,`. |
| `models` | body | `string` | no | Processing model (auto, tesseract, paddleocr, whisper*). |
| `ocr` | body | `string` | no | OCR control (auto, force, skip). |
| `webhookUrl` | body | `string` | no | Optional webhook URL for completion notifications. |
| `reference` | body | `string` | no | Optional client reference ID for tracking. |
| `jobExpiryInMinutes` | body | `number` | no | Optional job expiration time in minutes. |
| `response` | body | `string` | no | Response mode (polling, direct, webhook, persisted). |
