# Update Service with PagerDuty

## Endpoint

- **Method:** `PUT`
- **Path:** `/services/:id`
- **Base URL:** `https://api.pagerduty.com`
- **Official documentation:** [Update Service](https://developer.pagerduty.com/api-reference/updateService)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PagerDuty service ID to update. |
| `service.name` | body | `string` | no | The updated service name. |
| `service.description` | body | `string` | no | The updated service description. |
| `service.escalation_policy.id` | body | `string` | yes | The updated escalation policy ID. |
