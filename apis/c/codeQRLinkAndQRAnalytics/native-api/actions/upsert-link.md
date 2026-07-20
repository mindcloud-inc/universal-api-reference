# Upsert Link with CodeQR - Link and QR Analytics

Updates or creates a link in CodeQR.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/links/update`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Upsert Link](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The destination URL of the short link. |
| `title` | body | `string` | no | The title of the short link. |
