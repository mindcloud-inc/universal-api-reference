# Create WiFi QR Code with QR Api

Creates a QR code for Wi-Fi access in QR Api.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcode/wifi`
- **Base URL:** `https://qrapi.io/v2`
- **Official documentation:** [Create WiFi QR Code](https://qrapi.io/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ssid` | query | `string` | yes | Exact WiFi network name to encode. |
| `authentication` | query | `string` | no | WiFi authentication type. |
| `psk` | query | `string` | no | WiFi password or pre-shared key. |
| `size` | query | `string` | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. |
| `format` | query | `string` | no | QR code output format: png, jpg, svg, pdf, or eps. |
