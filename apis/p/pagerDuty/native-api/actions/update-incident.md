# Update Incident with PagerDuty

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/:id`
- **Base URL:** `https://api.pagerduty.com`
- **Official documentation:** [Update Incident](https://developer.pagerduty.com/api-reference/updateIncident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PagerDuty incident ID to update. |
| `incident.title` | body | `string` | no | The new incident title. |
| `incident.status` | body | `string` | no | The new incident status. |
| `incident.urgency` | body | `string` | no | The new incident urgency. |
| `incident.resolution` | body | `string` | no | Resolution note used when resolving an incident. |
| `incident.service.id` | body | `string` | no | The service ID to assign to the incident. |
