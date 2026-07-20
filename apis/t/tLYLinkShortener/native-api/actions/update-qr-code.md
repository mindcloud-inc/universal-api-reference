# Update QR Code with TLY Link Shortener

Updates a QR code in TLY Link Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/link/qr-code`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Update QR Code](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | body | `string` | yes | The short URL whose QR code should be updated. |
| `image` | body | `string` | no | Optional QR code image as a base64 data URL. |
| `background_color` | body | `string` | no | Optional background color for the QR code. |
| `corner_dots_color` | body | `string` | no | Optional corner dots color for the QR code. |
| `dots_color` | body | `string` | no | Optional dots color for the QR code. |
