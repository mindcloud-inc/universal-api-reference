# List Return Order Items with Returnless

Retrieves return order items from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/return-orders/{returnOrder}/items`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Return Order Items](https://docs.returnless.com/docs/api-rest-reference/b6c4c8fe65c93)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
