# Push Order with OrderOut

Pushes an order from a channel to OrderOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/channel/order/push`
- **Base URL:** `https://api.orderout.co`
- **Official documentation:** [Push Order](https://developers.orderout.co/reference/push-order-from-channel-to-orderout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RAW_BODY` | body | `string` | yes | Order payload JSON string |
