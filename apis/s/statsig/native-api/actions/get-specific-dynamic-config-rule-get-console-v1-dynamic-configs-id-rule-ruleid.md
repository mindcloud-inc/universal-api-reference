# Get Specific Dynamic Config Rule with Statsig

Retrieves a specific dynamic config rule from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/dynamic_configs/{id}/rule/{ruleId}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Specific Dynamic Config Rule](https://docs.statsig.com/api-reference/dynamic-configs/get-specific-dynamic-config-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Dynamic Config ID |
| `ruleId` | path | `string` | yes | Rule ID |
