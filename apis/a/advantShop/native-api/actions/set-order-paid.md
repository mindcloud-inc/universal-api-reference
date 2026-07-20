# Set Order Paid with AdvantShop

Marks an order as paid in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/setpaid`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Set Order Paid](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderId` | body | `number` | yes | Order identifier to mark paid. |
