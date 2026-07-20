# Update Gate Rules with Statsig

Updates gate rules in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/gates/{id}/rules/{ruleID}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Gate Rules](https://docs.statsig.com/api-reference/gates/update-gate-rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gate ID |
| `ruleID` | path | `string` | yes | Rule ID |
| `name` | body | `string` | no | Request body field. |
| `passPercentage` | body | `number` | no | Request body field. |
| `conditions` | body | `list` | no | Request body field. |
| `environments` | body | `list` | no | Request body field. |
| `baseID` | body | `string` | no | Request body field. |
| `returnValue` | body | `object` | no | Request body field. |
| `completedAutomatedRollouts` | body | `list` | no | Request body field. |
| `pendingAutomatedRollouts` | body | `list` | no | Request body field. |
| `conditions` | body | `object` | no | Request body field. |
