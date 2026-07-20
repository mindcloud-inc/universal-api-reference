# Get Pulse Load History Details (Warehouse Native) with Statsig

Retrieves warehouse-native pulse load history details from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/experiments/{id}/pulse_load_history/{dagID}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Pulse Load History Details (Warehouse Native)](https://docs.statsig.com/api-reference/experiments/get-pulse-load-history-details-warehouse-native)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `dagID` | path | `string` | yes | dagID |
