# Pull Orders with MarketTime

## Endpoint

- **Method:** `POST`
- **Path:** `/mtpublic/api/v1/:whoAmI/orders/get`
- **Base URL:** `https://publicapi.markettime.com`
- **Official documentation:** [Pull Orders](https://publicapi.markettime.com/swagger-ui/index.html#/Order/queryOrders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[]` | body | `array` | no | — |
| `filters[].field` | body | `list` | no | — |
| `excludeOrderDetails` | query | `boolean` | no | Exclude line details from the response. |
| `filters[].operator` | body | `string` | no | — |
| `filters[].value` | body | `string` | no | — |
