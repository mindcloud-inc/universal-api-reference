# Generate QR Code with 1001fx

Creates a QR code from text.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/generateqrcode`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Generate QR Code](https://1001fx.com/functions/generateqrcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backgroundColor` | body | `string` | no | Background color for the QR code image. |
| `errorCorrectionLevel` | body | `string` | no | Error correction level for the QR code. |
| `text` | body | `string` | yes | Text value to encode in the QR code. |
| `textColor` | body | `string` | no | Foreground color for the QR code image. |
| `width` | body | `number` | no | Width of the generated QR code image. |
