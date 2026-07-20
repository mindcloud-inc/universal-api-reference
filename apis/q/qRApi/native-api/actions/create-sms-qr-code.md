# Create SMS QR Code with QR Api

Creates a QR code for a prefilled SMS in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/SMS`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create SMS QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_no` | query | `string` | yes | Recipient phone number for the SMS QR code. |
| `message` | query | `string` | yes | SMS message to encode in the QR code. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
