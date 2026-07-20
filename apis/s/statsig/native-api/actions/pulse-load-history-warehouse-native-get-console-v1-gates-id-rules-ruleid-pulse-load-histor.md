# Pulse Load History (Warehouse Native) with Statsig

Retrieves warehouse-native pulse load history from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/gates/{id}/rules/{ruleID}/pulse_load_history`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Pulse Load History (Warehouse Native)](https://docs.statsig.com/api-reference/gates/pulse-load-history-warehouse-native)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gate ID |
| `ruleID` | path | `string` | yes | Rule ID |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
