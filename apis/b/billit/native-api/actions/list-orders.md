# List Orders with Billit

Retrieves Billit orders for the authenticated company.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [List Orders](https://docs.billit.be/reference/order_getorders-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter string for narrowing Billit orders. |
