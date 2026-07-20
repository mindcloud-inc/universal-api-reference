# List Incident Impacts with FireHydrant

Retrieves incident impacts by type from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/:incident_id/impact/:type`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Incident Impacts](https://docs.firehydrant.com/reference/list_incident_impacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `type` | path | `list` | yes | The impacted infrastructure type to list. Accepted values: `0`, `1`, `2`, `3`. |
