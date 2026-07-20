# List Domains with CodeQR - Link and QR Analytics

Retrieves domains from CodeQR.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [List Domains](https://docs.codeqr.io/api-reference/endpoint/retrieve-a-list-of-domains)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | The search term to filter the domains by. |
| `archived` | query | `boolean` | no | Whether to include archived domains in the response. |
