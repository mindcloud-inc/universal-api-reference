# List Incident Assignees with FireHydrant

Retrieves incident role assignments from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/:incident_id/role_assignments`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Incident Assignees](https://docs.firehydrant.com/reference/list_incident_role_assignments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `status` | query | `string` | no | Filter assignees by assignment status. |
