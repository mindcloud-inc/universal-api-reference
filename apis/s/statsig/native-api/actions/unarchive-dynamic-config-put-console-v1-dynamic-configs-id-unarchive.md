# Unarchive Dynamic Config with Statsig

Unarchives a dynamic config in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/dynamic_configs/{id}/unarchive`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Unarchive Dynamic Config](https://docs.statsig.com/api-reference/dynamic-configs/unarchive-dynamic-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `unarchiveReason` | body | `string` | no | Request body field. |
