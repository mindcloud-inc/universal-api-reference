# Change Order Status with AdvantShop

Updates an order status in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/changestatus`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Change Order Status](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderId` | body | `number` | yes | Order identifier to update. |
| `StatusId` | body | `number` | yes | Target order status identifier. |
