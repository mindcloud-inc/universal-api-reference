# Create Environment with ConfigCat

Creates a new environment in ConfigCat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/products/:productId/environments`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Create Environment](https://configcat.com/docs/api/reference/create-environment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The identifier of the Product. |
| `environment` | body | `object` | yes | Raw ConfigCat environment body. Create requires at least name. |
