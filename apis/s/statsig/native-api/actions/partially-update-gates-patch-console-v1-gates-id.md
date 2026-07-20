# Partially Update Gates with Statsig

Updates gates in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/gates/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Partially Update Gates](https://docs.statsig.com/api-reference/gates/partially-update-gates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `isEnabled` | body | `boolean` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `rules` | body | `list` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `type` | body | `string` | no | Request body field. |
| `idType` | body | `string` | no | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
| `creatorID` | body | `string` | no | Request body field. |
| `creatorEmail` | body | `string` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `measureMetricLifts` | body | `boolean` | no | Request body field. |
| `monitoringMetrics` | body | `list` | no | Request body field. |
| `reviewSettings` | body | `object` | no | Request body field. |
| `releasePipelineID` | body | `string` | no | Request body field. |
