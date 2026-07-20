# Create QR Code with Payrexx

Creates a QR code in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `QrCode/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Create QR Code](https://developers.payrexx.com/reference/create-a-qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | QR code amount in cents. |
| `currency` | body | `string` | yes | QR code currency. |
| `webshopUrl` | body | `string` | yes | Webshop URL for the QR code. |
