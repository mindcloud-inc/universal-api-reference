# Update Incident with Instatus

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:page_id/incidents/:incident_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Update Incident](https://instatus.com/help/api/incidents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Incident name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `status` | body | `string` | no | Incident status. |
| `incident_id` | path | `string` | yes | Instatus incident ID. |
