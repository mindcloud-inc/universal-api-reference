# Create Google Maps QR Code with QR Api

Creates a QR code for a Google Maps location in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/googlemaps`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create Google Maps QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Map location latitude in degrees. |
| `longitude` | query | `number` | yes | Map location longitude in degrees. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
