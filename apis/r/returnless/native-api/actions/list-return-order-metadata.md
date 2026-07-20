# List Return Order Metadata with Returnless

Retrieves return order metadata from Returnless.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-01/return-orders/{returnOrder}/meta-data`
- **Base URL:** `https://api-v2.returnless.com`
- **Official documentation:** [List Return Order Metadata](https://docs.returnless.com/docs/api-rest-reference/d88519cafe174)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `returnOrder` | path | `string` | yes | The unique identifier of the return order. |
