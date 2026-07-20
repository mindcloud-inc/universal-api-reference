# Get QR Code Image with Bitly

Retrieves a QR code image from Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/qr-codes/:qrcode_id/image`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Get QR Code Image](https://dev.bitly.com/api-reference#getQRCodeImagePublic)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `format` | query | `string` | no |
| `qrcode_id` | path | `string` | yes |
