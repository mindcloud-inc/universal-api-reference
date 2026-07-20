# Track Order Shipment with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/order/track`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Track Order Shipment](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-shipment-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_info` | body | `string` | yes | JSON object string describing the order and shipment links. |
