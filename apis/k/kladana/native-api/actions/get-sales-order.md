# Get Sales Order with Kladana

Retrieves a sales order from Kladana.

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/customerorder/{id}`
- **Base URL:** `https://api.kladana.com/api/remap/1.2`
- **Official documentation:** [Get Sales Order](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-sales-order-get-sales-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Kladana sales order ID from the Sales Order resource URL. |
