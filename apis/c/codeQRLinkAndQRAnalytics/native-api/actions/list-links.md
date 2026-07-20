# List Links with CodeQR - Link and QR Analytics

Retrieves links from CodeQR.

## Endpoint

- **Method:** `GET`
- **Path:** `/links`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [List Links](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectSlug` | query | `string` | no | The slug of the project to which the link belongs. |
| `domain` | query | `string` | no | The domain to filter the links. |
| `search` | query | `string` | no | The search term to filter the links by slug or destination URL. |
| `showArchived` | query | `boolean` | no | Whether to include archived links in the response. |
