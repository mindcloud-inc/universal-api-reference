# Get QR Code with OpenQR

Retrieves a QR code from the OpenQR account.

## Endpoint

- **Method:** `GET`
- **Path:** `/qr-codes/:qr_code_id`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Get QR Code](https://docs.openqr.io/#tag/QR-Codes/operation/ViewQRCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qr_code_id` | path | `string` | yes | QR Code ID. |
