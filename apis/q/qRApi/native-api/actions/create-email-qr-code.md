# Create Email QR Code with QR Api

Creates a QR code for an email address in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/email`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create Email QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Email address to encode in the QR code. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
