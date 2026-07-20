# Create Incident Update with Instatus

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:page_id/incidents/:incident_id/incident-updates`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Create Incident Update](https://instatus.com/help/api/incident-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Incident update message. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `status` | body | `string` | yes | Incident update status. |
| `incident_id` | path | `string` | yes | Instatus incident ID. |
| `components[]` | body | `array<string>` | yes | Affected component IDs. Send multiple values as a array. |
| `notify` | body | `boolean` | no | Whether to notify subscribers. |
| `statuses[]` | body | `array<object>` | yes | Statuses for each affected component. Include matching component IDs in Component IDs. Send multiple values as a array. |
