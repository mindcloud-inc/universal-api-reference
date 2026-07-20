# Create Order v2 with Gelato

Creates an order in Gelato v2 from a promise UID.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.gelato.com/v2/order/create`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Create Order v2](https://dashboard.gelato.com/docs/orders/v2/create/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `promiseUid` | body | `string` | yes |
