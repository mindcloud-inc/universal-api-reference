# List Configs with ConfigCat

Retrieves configs from a ConfigCat product.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products/:productId/configs`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [List Configs](https://configcat.com/docs/api/reference/get-configs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The identifier of the Product. |
