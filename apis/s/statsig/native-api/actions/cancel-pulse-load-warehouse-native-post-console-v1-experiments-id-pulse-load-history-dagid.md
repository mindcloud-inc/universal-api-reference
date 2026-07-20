# Cancel Pulse Load (Warehouse Native) with Statsig

Cancels a warehouse-native pulse load in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/pulse_load_history/{dagID}/cancel`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Cancel Pulse Load (Warehouse Native)](https://docs.statsig.com/api-reference/experiments/cancel-pulse-load-warehouse-native)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `dagID` | path | `string` | yes | dagID |
