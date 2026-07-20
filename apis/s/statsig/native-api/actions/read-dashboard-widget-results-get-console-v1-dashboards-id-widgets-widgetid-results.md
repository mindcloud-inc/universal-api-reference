# Read Dashboard Widget Results with Statsig

Retrieves dashboard widget results from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/dashboards/{id}/widgets/{widgetId}/results`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Dashboard Widget Results](https://docs.statsig.com/api-reference/dashboards/read-dashboard-widget-results)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | dashboard id |
| `widgetId` | path | `string` | yes | widget id |
| `sampling_enabled` | query | `boolean` | no | Whether funnel sampling should be enabled for this results query. Defaults to true. |
