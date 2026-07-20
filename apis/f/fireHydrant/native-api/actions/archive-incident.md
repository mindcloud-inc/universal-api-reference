# Archive Incident with FireHydrant

Archives an existing incident in FireHydrant.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/incidents/:incident_id`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [Archive Incident](https://docs.firehydrant.com/reference/delete_incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
