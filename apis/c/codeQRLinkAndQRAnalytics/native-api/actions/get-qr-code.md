# Get QR Code with CodeQR - Link and QR Analytics

Retrieves a QR code from CodeQR.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcodes/info`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Get QR Code](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | query | `string` | yes | The external ID of the QR code prefixed with ext_ when used as a query parameter. |
| `projectSlug` | query | `string` | no | The slug of the project to which the QR code belongs. |
| `domain` | query | `string` | no | The domain of the QR code to retrieve. |
| `qrCodeId` | query | `string` | no | The unique ID of the QR code. |
| `key` | query | `string` | no | The key of the QR code to retrieve. |
