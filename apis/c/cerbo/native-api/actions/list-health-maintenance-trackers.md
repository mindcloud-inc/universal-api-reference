# List Health Maintenance Trackers with Cerbo

Retrieves health maintenance trackers from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/health_maintenance`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Health Maintenance Trackers](https://docs.cer.bo/#tag/Health-Maintenance/operation/listHealthMaintenance)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_specific_pt` | query | `boolean` | no | If set, returns specific patient data. |
