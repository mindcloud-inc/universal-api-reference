# Create Stock Corrections with Brightpearl

## Endpoint

- **Method:** `POST`
- **Path:** `/warehouse-service/warehouse/:warehouseId/stock-correction`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Create Stock Corrections](https://api-docs.brightpearl.com/warehouse/stock-correction/post.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `warehouseId` | path | `number` | yes | — |
| `corrections[]` | body | `array<object>` | yes | — |
| `corrections[].quantity` | body | `number` | yes | Positive adds stock; negative removes stock. |
| `corrections[].productId` | body | `number` | yes | — |
| `corrections[].reason` | body | `string` | yes | — |
| `corrections[].locationId` | body | `number` | yes | Use location 2 for standard inventory management. |
| `corrections[].cost` | body | `object` | no | Required when adding stock. |
| `corrections[].cost.currency` | body | `string` | no | Required when adding stock. |
| `corrections[].cost.value` | body | `number` | no | Per-item cost. Required when adding stock. |
| `corrections[].batchId` | body | `number` | no | Only for removing stock. Omit to use FIFO. |
| `corrections[].orderId` | body | `number` | no | — |
