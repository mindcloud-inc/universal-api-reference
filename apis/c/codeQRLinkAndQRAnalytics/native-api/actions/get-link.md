# Get Link with CodeQR - Link and QR Analytics

Retrieves a link from CodeQR.

## Endpoint

- **Method:** `GET`
- **Path:** `/links/info`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Get Link](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectSlug` | query | `string` | yes | The slug of the project to which the link belongs. |
| `domain` | query | `string` | yes | The domain of the link to retrieve. |
| `key` | query | `string` | yes | The key of the link to retrieve. |
