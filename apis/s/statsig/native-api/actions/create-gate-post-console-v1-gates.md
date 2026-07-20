# Create Gate with Statsig

Creates a gate in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/gates`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Gate](https://docs.statsig.com/api-reference/gates/create-gate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
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
| `id` | body | `string` | no | Request body field. |
| `isTemplate` | body | `boolean` | no | Request body field. |
