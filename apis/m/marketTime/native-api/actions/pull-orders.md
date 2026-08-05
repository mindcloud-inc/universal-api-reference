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
| `excludeOrderDetails` | query | `boolean` | no | Exclude line details from the response. |
