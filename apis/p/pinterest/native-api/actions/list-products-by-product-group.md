# List Products By Product Group with Pinterest

Retrieves product pins from a Pinterest product group.

## Endpoint

- **Method:** `GET`
- **Path:** `catalogs/product_groups/:productGroupId/products`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [List Products By Product Group](https://developers.pinterest.com/docs/api/v5/#operation/catalogs_product_group_pins/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productGroupId` | path | `string` | no |
