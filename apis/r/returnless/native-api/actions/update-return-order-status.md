# Update Return Order Status with Returnless

Updates a return order status in Returnless.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/2025-01/return-orders/{returnOrder}/status`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Update Return Order Status](https://docs.returnless.com/docs/api-rest-reference/1d07e272437a4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
