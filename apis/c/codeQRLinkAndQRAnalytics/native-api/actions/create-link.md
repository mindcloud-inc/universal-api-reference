# Create Link with CodeQR - Link and QR Analytics

Creates a link in CodeQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/links`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Create Link](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The destination URL of the short link. |
| `externalId` | body | `string` | no | The external ID for the link in your system. |
