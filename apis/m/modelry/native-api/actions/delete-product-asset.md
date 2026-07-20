# Delete Product Asset with Modelry

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/products/:product_id/assets/:id`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Delete Product Asset](https://files.cgtarsenal.com/api/doc/index.html#api-ProductAssets-DeleteProductAsset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | Modelry product ID. |
| `id` | path | `number` | yes | Modelry product asset ID. |
