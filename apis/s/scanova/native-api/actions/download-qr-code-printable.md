# Download QR Code (Printable) with Scanova

## Endpoint

- **Method:** `POST`
- **Path:** `/qr/download/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Download QR Code (Printable)](https://docs.scanova.io/api-reference/endpoint/qr_manager/download-printable)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrid` | body | `string` | yes | QR code ID |
| `name` | body | `string` | no | Name for the downloaded file |
| `for_print` | body | `string` | yes | Must be set to 'true' for printable format |
| `size` | body | `string` | no | Size of the QR code in pixels (300-600px) |
