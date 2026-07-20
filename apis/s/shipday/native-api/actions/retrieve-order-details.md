# Retrieve Order Details with Shipday

Retrieves order details from Shipday.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:orderNumber`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Retrieve Order Details](https://docs.shipday.com/reference/retrieve-order-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ordernumber` | path | `string` | yes | Shipday order reference used in the request path. |
