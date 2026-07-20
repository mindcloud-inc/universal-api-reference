# Retrieve Order Details with GoDaddy CRM

Retrieves order details from your GoDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/:orderId`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Retrieve Order Details](https://developer.godaddy.com/doc/endpoint/orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order ID whose details should be retrieved. |
