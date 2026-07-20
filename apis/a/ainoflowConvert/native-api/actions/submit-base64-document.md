# Submit Base64 Document with Ainoflow Convert

Creates a conversion job in Ainoflow Convert from base64 content.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/convert/submit-base64`
- **Base URL:** `https://api.ainoflow.io`
- **Official documentation:** [Submit Base64 Document](https://www.ainoflow.io/docs/api/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentBase64` | body | `string` | yes | Base64-encoded file content. |
| `filename` | body | `string` | no | Original filename for content type detection. |
| `languages` | body | `string` | yes | Comma-separated language codes. Send multiple values as a string separated by `,`. |
| `outputs` | body | `string` | yes | Comma-separated output formats. Send multiple values as a string separated by `,`. |
| `models` | body | `string` | no | Processing model (default: auto). |
| `response` | body | `string` | no | Response mode (default: polling). |
