# Update Order Status with Dukaan

Updates an order status in Dukaan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/order/seller/:orderUuid/order/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Update Order Status](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderUuid` | path | `string` | yes | Dukaan order UUID. |
| `status` | body | `number` | yes | Dukaan order status code. |
