# Archive Dynamic Config with Statsig

Archives a dynamic config in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/dynamic_configs/{id}/archive`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Archive Dynamic Config](https://docs.statsig.com/api-reference/dynamic-configs/archive-dynamic-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `forceArchive` | body | `boolean` | no | Request body field. |
| `archiveReason` | body | `string` | no | Request body field. |
