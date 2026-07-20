# Publish Product Embed with Modelry

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/products/:product_id/embeds/:id/publish`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Publish Product Embed](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-PublishProductViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `number` | yes | Modelry product ID. |
| `id` | path | `number` | yes | Modelry embed ID. |
