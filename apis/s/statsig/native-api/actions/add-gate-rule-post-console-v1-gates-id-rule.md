# Add Gate Rule with Statsig

Adds gate rule in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/gates/{id}/rule`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Add Gate Rule](https://docs.statsig.com/api-reference/gates/add-gate-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | yes | Request body field. |
| `passPercentage` | body | `number` | yes | Request body field. |
| `conditions` | body | `list` | yes | Request body field. |
| `environments` | body | `list` | no | Request body field. |
| `baseID` | body | `string` | no | Request body field. |
| `returnValue` | body | `object` | no | Request body field. |
| `completedAutomatedRollouts` | body | `list` | no | Request body field. |
| `pendingAutomatedRollouts` | body | `list` | no | Request body field. |
