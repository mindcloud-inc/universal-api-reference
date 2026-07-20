# Create Phone Call QR Code with QR Api

Creates a QR code for a phone call in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/phonecall`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create Phone Call QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | Phone number to encode in the QR code. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
