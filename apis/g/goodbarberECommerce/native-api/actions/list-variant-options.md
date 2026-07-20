# List Variant Options with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/option/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List Variant Options](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Restricts the list of returned options to the ones whose name contains the provided argument. |
