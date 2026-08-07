# List assets with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/assets`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List assets](https://developer-docs.gomotive.com/reference/list-all-the-company-assets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter assets by name. |
| `status` | query | `string` | no | Filter assets by status. |
| `exact_match` | query | `boolean` | no | Require exact-casing name matches. |
