# Update Incident Update with Instatus

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:page_id/incidents/:incident_id/incident-updates/:incident_update_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Update Incident Update](https://instatus.com/help/api/incident-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Incident update message. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `incident_id` | path | `string` | yes | Instatus incident ID. |
| `incident_update_id` | path | `string` | yes | Instatus incident update ID. |
| `started` | body | `string` | yes | Date and time when this incident update happened. |
| `status` | body | `string` | no | Incident update status. |
| `notify` | body | `boolean` | no | Whether to notify subscribers. |
| `components[]` | body | `array<string>` | no | IDs of affected components. Send multiple values as a array. |
| `statuses[]` | body | `array<object>` | no | Statuses for each affected component. Include matching component IDs in Component IDs. Send multiple values as a array. |
