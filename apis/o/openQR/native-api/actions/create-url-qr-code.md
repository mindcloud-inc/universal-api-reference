# Create URL QR Code with OpenQR

Creates a URL QR code in OpenQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr-codes`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Create URL QR Code](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | QR code name. |
| `data.url` | body | `string` | yes | URL to encode in the QR code. Maximum length: 350. |
