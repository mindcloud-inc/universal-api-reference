# Reject Return Order with Returnless

Rejects a return order in Returnless.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-01/return-orders/{returnOrder}/reject`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Reject Return Order](https://docs.returnless.com/docs/api-rest-reference/e5d201fe70527)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
