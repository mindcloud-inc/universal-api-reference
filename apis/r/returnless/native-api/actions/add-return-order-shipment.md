# Add Return Order Shipment with Returnless

Adds a shipment to a return order in Returnless.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-01/return-orders/{returnOrder}/shipments`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Add Return Order Shipment](https://docs.returnless.com/docs/api-rest-reference/455a6fbc1d4eb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
