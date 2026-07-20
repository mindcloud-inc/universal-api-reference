# List Purchase Orders with Bexio

Retrieves purchase orders from Bexio.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0/purchase_orders`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [List Purchase Orders](https://docs.bexio.com/#tag/Purchase-Orders/operation/v3PurchaseOrderList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_by` | query | `list<string>` | no | Defines the order of the results. Multiple sort parameters can be combined with a comma separator. `_asc` and `_desc` can be appended to any parameter to sort ascending or descending. Accepted values: `id`, `total`, `total_gross`, `total_net`, `updated_at`. |
