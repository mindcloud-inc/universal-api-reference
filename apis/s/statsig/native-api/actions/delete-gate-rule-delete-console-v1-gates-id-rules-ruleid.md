# Delete Gate Rule with Statsig

Deletes a gate rule from Statsig.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/console/v1/gates/{id}/rules/{ruleID}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Delete Gate Rule](https://docs.statsig.com/api-reference/gates/delete-gate-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gate ID |
| `ruleID` | path | `string` | yes | Rule ID |
