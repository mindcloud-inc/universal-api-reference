# Update Dynamic Config Rule By Id with Statsig

Updates a dynamic config rule in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/dynamic_configs/{id}/rule/{ruleId}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Dynamic Config Rule By Id](https://docs.statsig.com/api-reference/dynamic-configs/update-dynamic-config-rule-by-id)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Dynamic Config ID |
| `ruleId` | path | `string` | yes | Rule ID |
| `dryRun` | query | `boolean` | no | Skips persisting updates to the entity (used to validate that inputs are correct) |
| `name` | body | `string` | no | Request body field. |
| `passPercentage` | body | `number` | no | Request body field. |
| `conditions` | body | `list` | no | Request body field. |
| `environments` | body | `list` | no | Request body field. |
| `baseID` | body | `string` | no | Request body field. |
| `returnValue` | body | `object` | no | Request body field. |
| `completedAutomatedRollouts` | body | `list` | no | Request body field. |
| `pendingAutomatedRollouts` | body | `list` | no | Request body field. |
| `returnValueJson5` | body | `string` | no | Request body field. |
| `variants` | body | `list` | no | Request body field. |
