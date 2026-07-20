# Add Return Order Note with Returnless

Adds a note to a return order in Returnless.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-01/return-orders/{returnOrder}/notes`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Add Return Order Note](https://docs.returnless.com/docs/api-rest-reference/1aa005cc39ee0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
