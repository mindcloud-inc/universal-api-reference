# Create Product Category with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/InsertProductCategory`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Create Product Category](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | body | `number` | yes | Bot identifier. |
| `categoryName` | body | `string` | yes | Category name. |
| `description` | body | `string` | no | Category description. |
| `isActive` | body | `boolean` | no | Whether the category is active. |
| `isPopular` | body | `boolean` | no | Whether the category is popular. |
