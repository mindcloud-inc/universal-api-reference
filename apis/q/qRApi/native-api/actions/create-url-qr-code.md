# Create URL QR Code with QR Api

Creates a QR code for a URL in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/url`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create URL QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to encode in the QR code. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
