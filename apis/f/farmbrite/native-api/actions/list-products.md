# List products with Farmbrite

Retrieves a list of products from Farmbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.farmbrite.com/v1`
- **Official documentation:** [List products](https://developers.farmbrite.com/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | — |
| `limit` | query | `number` | no | — |
| `sort_by` | query | `string` | no | — |
| `sort_dir` | query | `list` | no | Accepted values: `Ascending`, `Descending`. |
