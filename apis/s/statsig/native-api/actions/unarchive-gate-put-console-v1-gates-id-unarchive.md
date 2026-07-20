# Unarchive Gate with Statsig

Unarchives a gate in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/gates/{id}/unarchive`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Unarchive Gate](https://docs.statsig.com/api-reference/gates/unarchive-gate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `unarchiveReason` | body | `string` | no | Request body field. |
