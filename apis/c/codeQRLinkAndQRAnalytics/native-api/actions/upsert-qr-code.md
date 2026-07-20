# Upsert QR Code with CodeQR - Link and QR Analytics

Updates or creates a QR code in CodeQR.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/qrcodes/upsert`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Upsert QR Code](https://docs.codeqr.io/api-reference/endpoint/upsert-a-qrcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The type of content of the QR code. |
| `url` | body | `string` | no | The destination URL of the QR code. |
| `title` | body | `string` | no | The title of the QR code. |
