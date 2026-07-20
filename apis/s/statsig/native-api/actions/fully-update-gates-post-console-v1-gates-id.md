# Fully Update Gates with Statsig

Updates gates in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/gates/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Fully Update Gates](https://docs.statsig.com/api-reference/gates/fully-update-gates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `isEnabled` | body | `boolean` | yes | Request body field. |
| `description` | body | `string` | yes | Request body field. |
| `rules` | body | `list` | yes | Request body field. |
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
