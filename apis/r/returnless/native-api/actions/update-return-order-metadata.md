# Update Return Order Metadata with Returnless

Updates return order metadata in Returnless.

## Endpoint

- **Method:** `PUT`
- **Path:** `/2025-01/return-orders/{returnOrder}/meta-data`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [Update Return Order Metadata](https://docs.returnless.com/docs/api-rest-reference/90f9683baeca5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
