# Attach Return Order Tags with Returnless

Attaches tags to a return order in Returnless.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-01/return-orders/{returnOrder}/tags`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Attach Return Order Tags](https://docs.returnless.com/docs/api-rest-reference/1303b1f885b0a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
