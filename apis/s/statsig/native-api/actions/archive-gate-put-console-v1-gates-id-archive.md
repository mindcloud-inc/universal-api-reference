# Archive Gate with Statsig

Archives a gate in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/gates/{id}/archive`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Archive Gate](https://docs.statsig.com/api-reference/gates/archive-gate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `forceArchive` | body | `boolean` | no | Request body field. |
| `archiveReason` | body | `string` | no | Request body field. |
