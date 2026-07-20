# Create Text QR Code with QR Api

Creates a QR code for plain text in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/text`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create Text QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | query | `string` | yes | Text to encode in the QR code. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
