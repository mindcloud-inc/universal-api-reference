# Update Shipment with Big Cartel

Updates a shipment for a Big Cartel order.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/orders/[:order-id]/shipments/[:shipment-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Update Shipment](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `order-id` | path | `string` | yes | The Big Cartel order ID. |
| `shipment-id` | path | `string` | yes | The Big Cartel shipment ID. |
