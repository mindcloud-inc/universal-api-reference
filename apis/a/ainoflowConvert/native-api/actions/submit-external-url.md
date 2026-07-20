# Submit External URL with Ainoflow Convert

Creates a conversion job in Ainoflow Convert from an external URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/convert/submit-url`
- **Base URL:** `https://api.ainoflow.io`
- **Official documentation:** [Submit External URL](https://www.ainoflow.io/docs/api/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceUrl` | body | `string` | yes | URL to download the file from. |
| `languages` | body | `string` | yes | Comma-separated language codes. Send multiple values as a string separated by `,`. |
| `outputs` | body | `string` | yes | Comma-separated output formats. Send multiple values as a string separated by `,`. |
| `models` | body | `string` | no | Processing model (default: auto). |
| `response` | body | `string` | no | Response mode (default: polling). |
