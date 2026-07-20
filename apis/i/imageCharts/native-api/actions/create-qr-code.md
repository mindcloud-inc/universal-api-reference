# Create QR Code with Image-Charts

Creates a QR code image with Image-Charts.

## Endpoint

- **Method:** `GET`
- **Path:** `/chart`
- **Base URL:** `https://image-charts.com`
- **Official documentation:** [Create QR Code](https://documentation.image-charts.com/qr-codes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chs` | query | `string` | yes | Image size in pixels as widthxheight, for example 150x150. |
| `chl` | query | `string` | yes | Text or URL to encode in the QR code. |
| `choe` | query | `string` | no | Character encoding used for QR payload text. |
