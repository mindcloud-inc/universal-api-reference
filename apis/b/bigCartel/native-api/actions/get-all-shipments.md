# Get All Shipments with Big Cartel

Retrieves shipments from a Big Cartel order.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/[:account-id]/orders/[:order-id]/shipments`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Get All Shipments](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `order-id` | path | `string` | yes | The Big Cartel order ID. |
