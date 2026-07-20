# Update QR Code with CodeQR - Link and QR Analytics

Updates a QR code in CodeQR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/qrcodes/:qrcodeId`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Update QR Code](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrcodeId` | path | `string` | yes | The ID of the QR code to update. |
| `url` | body | `string` | no | The destination URL for the QR code. |
