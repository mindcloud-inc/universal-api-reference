# List QR Codes with CodeQR - Link and QR Analytics

Retrieves QR codes from CodeQR.

## Endpoint

- **Method:** `GET`
- **Path:** `/qrcodes`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [List QR Codes](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectSlug` | query | `string` | no | The slug of the project to which the QR code belongs. |
| `domain` | query | `string` | no | The domain to filter the QR codes. |
| `search` | query | `string` | no | The search term to filter the QR codes by slug or destination URL. |
| `showArchived` | query | `boolean` | no | Whether to include archived QR codes in the response. |
