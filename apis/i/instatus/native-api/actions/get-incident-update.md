# Get Incident Update with Instatus

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:page_id/incidents/:incident_id/incident-updates/:incident_update_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Get Incident Update](https://instatus.com/help/api/incident-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `incident_id` | path | `string` | yes | Instatus incident ID. |
| `incident_update_id` | path | `string` | yes | Instatus incident update ID. |
