# List Return Order Shipments with Returnless

Retrieves return order shipments from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/return-orders/{returnOrder}/shipments`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Return Order Shipments](https://docs.returnless.com/docs/api-rest-reference/1e0748fdd876f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
