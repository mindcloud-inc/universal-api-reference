# Create QR Code with goQR.me

Creates a QR code with goQR.me.

## Endpoint

- **Method:** `GET`
- **Path:** `/create-qr-code/`
- **Base URL:** `https://api.qrserver.com/v1`
- **Official documentation:** [Create QR Code](https://goqr.me/api/doc/create-qr-code/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | query | `string` | yes | Text to encode in the QR code. |
| `size` | query | `string` | no | Generated QR code size in pixels. |
| `charset-source` | query | `list<string>` | no | Charset used to encode the input text. Accepted values: `ISO-8859-1`, `UTF-8`. |
| `charset-target` | query | `list<string>` | no | Charset to store inside the QR code. Accepted values: `ISO-8859-1`, `UTF-8`. |
| `ecc` | query | `list<string>` | no | QR error correction level. Accepted values: `H`, `L`, `M`, `Q`. |
| `color` | query | `string` | no | QR data-module color. |
| `bgcolor` | query | `string` | no | QR background color. |
| `margin` | query | `number` | no | Pixel margin around the QR code. |
| `qzone` | query | `number` | no | Quiet zone around the QR code. |
| `format` | query | `list<string>` | no | File format for the generated QR code image. Accepted values: `eps`, `gif`, `jpeg`, `jpg`, `png`, `svg`. |
