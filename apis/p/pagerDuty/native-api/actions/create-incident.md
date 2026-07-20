# Create Incident with PagerDuty

## Endpoint

- **Method:** `POST`
- **Path:** `/incidents`
- **Base URL:** `https://api.pagerduty.com`
- **Official documentation:** [Create Incident](https://developer.pagerduty.com/api-reference/createIncident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident.title` | body | `string` | yes | A short description of the incident. |
| `incident.service.id` | body | `string` | yes | The PagerDuty service ID for the incident. |
| `incident.urgency` | body | `string` | no | The incident urgency. |
| `incident.incident_key` | body | `string` | no | A de-duplication key for the incident. |
