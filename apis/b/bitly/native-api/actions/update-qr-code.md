# Update QR Code with Bitly

Updates an existing QR code in Bitly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/qr-codes/:qrcode_id`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Update QR Code](https://dev.bitly.com/api-reference#updateQRCodePublic)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `qrcode_id` | path | `string` | yes |
| `title` | body | `string` | no |
