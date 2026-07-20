# List Sales Order Items with Returnless

Retrieves sales order items from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/sales-orders/{salesOrder}/items`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Sales Order Items](https://docs.returnless.com/docs/api-rest-reference/6b3c26dad0434)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesOrder` | path | `string` | yes | The unique identifier of the sales order. |
