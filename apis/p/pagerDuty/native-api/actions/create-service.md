# Create Service with PagerDuty

## Endpoint

- **Method:** `POST`
- **Path:** `/services`
- **Base URL:** `https://api.pagerduty.com`
- **Official documentation:** [Create Service](https://developer.pagerduty.com/api-reference/createService)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service.name` | body | `string` | no | The service name. |
| `service.description` | body | `string` | no | A description of the service. |
| `service.escalation_policy.id` | body | `string` | yes | The escalation policy ID for the service. |
