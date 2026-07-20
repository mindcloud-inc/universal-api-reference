# Fetch Order with Chargeblast

Retrieves an order from Chargeblast.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orders/:id`
- **Base URL:** `https://api.chargeblast.com`
- **Official documentation:** [Fetch Order](https://docs.chargeblast.com/api-reference/sync-data/get-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Chargeblast order ID to fetch. |
