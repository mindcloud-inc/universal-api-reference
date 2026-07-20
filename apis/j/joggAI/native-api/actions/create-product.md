# Create Product with JoggAI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/product`
- **Base URL:** `https://api.jogg.ai`
- **Official documentation:** [Create Product](https://docs.jogg.ai/api-reference/v2/Product/CreateProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Product description used for video generation context. |
| `name` | body | `string` | no | Product name. Required when no product URL is provided. |
| `target_audience` | body | `string` | no | Audience description to improve generated copy. |
| `url` | body | `string` | no | Public product URL to analyze. Required when no product name is provided. |
