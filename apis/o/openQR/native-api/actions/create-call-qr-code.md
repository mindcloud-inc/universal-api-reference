# Create Call QR Code with OpenQR

Creates a call QR code in OpenQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr-codes`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Create Call QR Code](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | QR code name. |
| `data.phone` | body | `string` | yes | Phone number to encode. Maximum length: 32. |
