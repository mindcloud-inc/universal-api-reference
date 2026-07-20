# Set Product Category Active Status with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/EditProductCategoryActiveStatus`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Set Product Category Active Status](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Category identifier. |
| `isActive` | body | `boolean` | yes | Whether the category is active. |
