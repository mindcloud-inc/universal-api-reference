# List Return Order Tags with Returnless

Retrieves return order tags from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/return-orders/{returnOrder}/tags`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Return Order Tags](https://docs.returnless.com/docs/api-rest-reference/d4d37e2232a35)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
