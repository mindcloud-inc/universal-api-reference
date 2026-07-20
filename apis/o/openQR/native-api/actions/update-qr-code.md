# Update QR Code with OpenQR

Updates an existing QR code in OpenQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr-codes/:qr_code_id`
- **Base URL:** `https://api.openqr.io/api/v1`
- **Official documentation:** [Update QR Code](https://docs.openqr.io/#tag/QR-Codes/operation/UpdateQRCode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qr_code_id` | path | `string` | yes | QR Code ID. |
| `name` | body | `string` | yes | QR code name. |
| `type` | body | `list` | yes | QR code type. Accepted values: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `data` | body | `object` | yes | Type-specific QR code data object. |
