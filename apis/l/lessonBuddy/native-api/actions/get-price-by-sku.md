# Get Price By SKU with LessonBuddy

Retrieves a product price in LessonBuddy by SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ims/inventory/:locationId/price-by-sku/:sku`
- **Base URL:** `https://api.lessonbuddy.com`
- **Official documentation:** [Get Price By SKU](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `number` | yes | LessonBuddy location ID. |
| `sku` | path | `string` | yes | Inventory SKU. |
