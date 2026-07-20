# Create Product Embed with Modelry

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/products/:product_id/embeds`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Create Product Embed](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-CreateProductViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | Modelry product ID. |
| `product_viewer.title` | body | `string` | yes | Embed title. |
| `product_viewer.kinds[]` | body | `array<string>` | yes | Embed kinds array. |
| `product_viewer.blob_ids[]` | body | `array<string>` | yes | Signed blob IDs. |
| `product_viewer.product_asset_ids[]` | body | `array<number>` | yes | Product asset IDs. |
