# Create Static Text QR Code with OpenQR

Creates a static text QR code in OpenQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr-codes`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Create Static Text QR Code](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | QR code name. |
| `data.text` | body | `string` | yes | Text to encode in the QR code. Maximum length: 350. |
