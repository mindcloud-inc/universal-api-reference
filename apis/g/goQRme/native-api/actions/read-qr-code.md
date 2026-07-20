# Read QR Code with goQR.me

Reads a QR code with goQR.me.

## Endpoint

- **Method:** `POST`
- **Path:** `/read-qr-code/`
- **Base URL:** `https://api.qrserver.com/v1`
- **Official documentation:** [Read QR Code](https://goqr.me/api/doc/read-qr-code/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileurl` | query | `string` | no | URL of a publicly reachable QR code image. |
| `file` | body | `file` | no | Upload a QR code image file. |
| `outputformat` | query | `list<string>` | no | Response format for the scan result. Accepted values: `JSON`, `XML`. |
