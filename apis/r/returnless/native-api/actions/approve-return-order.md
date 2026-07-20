# Approve Return Order with Returnless

Approves a return order in Returnless.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-01/return-orders/{returnOrder}/approve`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Approve Return Order](https://docs.returnless.com/docs/api-rest-reference/c3a41f4317680)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
