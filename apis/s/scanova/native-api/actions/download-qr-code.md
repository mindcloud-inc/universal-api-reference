# Download QR Code with Scanova

## Endpoint

- **Method:** `GET`
- **Path:** `/qr/{qrid}/download/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Download QR Code](https://docs.scanova.io/api-reference/endpoint/qr_manager/download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrid` | path | `string` | yes | QR Code ID |
| `file` | query | `string` | no | Download format |
| `size` | query | `number` | no | Size of the QR code image in pixels (width and height). Must be between 10 and 1000 pixels. |
| `for_print` | query | `boolean` | no | When true, returns a print-optimized QR code (e.g. black and white, suitable for professional printing). |
