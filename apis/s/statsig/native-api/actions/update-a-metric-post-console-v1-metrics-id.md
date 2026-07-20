# Update a metric with Statsig

Updates a metric in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/metrics/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update a metric](https://docs.statsig.com/api-reference/metrics/update-a-metric)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `isVerified` | body | `boolean` | no | Request body field. |
| `isReadOnly` | body | `boolean` | no | Request body field. |
| `isPermanent` | body | `boolean` | no | Request body field. |
| `warehouseNative` | body | `object` | no | Request body field. |
| `unitTypes` | body | `list` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `directionality` | body | `string` | no | Request body field. |
| `dryRun` | body | `boolean` | no | Request body field. |
| `owner` | body | `object` | no | Request body field. |
