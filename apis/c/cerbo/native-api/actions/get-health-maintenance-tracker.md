# Get Health Maintenance Tracker with Cerbo

Retrieves health maintenance tracker details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/health_maintenance/:health_maintenance_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Health Maintenance Tracker](https://docs.cer.bo/#tag/Health-Maintenance/operation/showHealthMaintenance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `health_maintenance_id` | path | `number` | yes | The ID of the health maintenance tracker to retrieve. |
