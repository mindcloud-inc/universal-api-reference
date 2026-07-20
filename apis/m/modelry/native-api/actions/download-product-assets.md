# Download Product Assets with Modelry

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products/:product_id/assets/download`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Download Product Assets](https://files.cgtarsenal.com/api/doc/index.html#api-ProductAssets-DownloadProductAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | Modelry product ID. |
| `source_file` | query | `boolean` | no | Only source files. |
