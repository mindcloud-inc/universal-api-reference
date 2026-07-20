# Delete Dynamic Config Rule with Statsig

Deletes a dynamic config rule from Statsig.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/console/v1/dynamic_configs/{id}/rule/{ruleId}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Delete Dynamic Config Rule](https://docs.statsig.com/api-reference/dynamic-configs/delete-dynamic-config-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Dynamic Config ID |
| `ruleId` | path | `string` | yes | Rule ID |
