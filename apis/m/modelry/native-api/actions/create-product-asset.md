# Create Product Asset with Modelry

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/products/:product_id/assets`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Create Product Asset](https://files.cgtarsenal.com/api/doc/index.html#api-ProductAssets-CreateProductAsset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | Modelry product ID. |
| `blob_id` | body | `string` | yes | Signed blob ID from upload. |
| `tags[]` | body | `array<string>` | yes | Asset tags. |
