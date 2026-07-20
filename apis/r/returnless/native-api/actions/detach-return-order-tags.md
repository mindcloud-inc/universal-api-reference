# Detach Return Order Tags with Returnless

Detaches tags from a return order in Returnless.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/2025-01/return-orders/{returnOrder}/tags`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Detach Return Order Tags](https://docs.returnless.com/docs/api-rest-reference/13505cb7e1fbe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
| `tags[]` | query | `array<string>` | yes | The array of tag IDs to detach from the return order. |
