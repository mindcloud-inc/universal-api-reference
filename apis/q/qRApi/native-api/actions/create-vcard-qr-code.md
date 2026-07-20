# Create VCard QR Code with QR Api

Creates a QR code for a vCard in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/vcard`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create VCard QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uname` | query | `string` | yes | Full name of the contact to encode in the vCard QR code. |
| `title` | query | `string` | no | Contact title or designation. |
| `company` | query | `string` | no | Contact company name. |
| `email` | query | `string` | no | Contact email address. |
| `phone` | query | `string` | no | Contact phone number. |
| `website` | query | `string` | no | Contact website URL. |
| `street` | query | `string` | no | Contact street address. |
| `city` | query | `string` | no | Contact city. |
| `country` | query | `string` | no | Contact country. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
