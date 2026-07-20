# Delete Shipment with Big Cartel

Deletes a shipment from a Big Cartel order.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/accounts/[:account-id]/orders/[:order-id]/shipments/[:shipment-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Delete Shipment](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `order-id` | path | `string` | yes | The Big Cartel order ID. |
| `shipment-id` | path | `string` | yes | The Big Cartel shipment ID. |
