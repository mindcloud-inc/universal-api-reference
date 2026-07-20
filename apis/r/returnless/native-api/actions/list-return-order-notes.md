# List Return Order Notes with Returnless

Retrieves return order notes from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/return-orders/{returnOrder}/notes`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Return Order Notes](https://docs.returnless.com/docs/api-rest-reference/71b1c8cd85421)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
