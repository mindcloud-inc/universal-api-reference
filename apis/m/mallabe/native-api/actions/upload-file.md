# Upload File with Mallabe

Uploads a file to Mallabe for hosting.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/upload`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Upload File](https://rapidapi.com/mallabe1/api/mallabe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Publicly accessible file URL. |
| `base64File` | body | `string` | no | Base64-encoded file data. |
| `webhookUrl` | body | `string` | no | Webhook URL for asynchronous callbacks. |
| `fileName` | body | `string` | no | Output file name without extension. |
| `fileExtension` | body | `string` | no | Output file extension. |
