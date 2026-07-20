# Create QR Code with CodeQR - Link and QR Analytics

Creates a QR code in CodeQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/qrcodes`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Create QR Code](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The type of content of the QR code. |
| `url` | body | `string` | yes | The destination URL of the QR code when using type url. |
| `externalId` | body | `string` | no | The external ID for the QR code in your system. |
