# List Products with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/catalog/:webzine_id/product/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List Products](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Restricts the list of returned products to the ones whose title, summary, description, tags, SKU, or slug contains the provided argument. Use comma-separated values to match A OR B. |
| `status` | query | `string` | no | Restricts the list of returned products to a certain publishing status. |
