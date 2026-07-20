# Get QR Code with TLY Link Shortener

Retrieves a QR code from TLY Link Shortener.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/link/qr-code`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Get QR Code](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | query | `string` | yes | The short URL to generate the QR code for. |
| `output` | query | `string` | no | Optional response format such as image or base64. |
