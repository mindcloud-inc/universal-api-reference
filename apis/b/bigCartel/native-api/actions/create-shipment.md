# Create Shipment with Big Cartel

Creates a shipment for a Big Cartel order.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/[:account-id]/orders/[:order-id]/shipments`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Create Shipment](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `order-id` | path | `string` | yes | The Big Cartel order ID. |
