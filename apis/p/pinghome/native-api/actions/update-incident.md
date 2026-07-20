# Update Incident with Pinghome

Updates an existing incident in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incident-cmd/v1/incident/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Incident](https://docs.pinghome.io/incident-management/incident-tracking/update-incident/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Incident ID to update. |
| `status` | body | `string` | no | Incident lifecycle status. |
| `name` | body | `string` | yes | Updated incident name. |
| `description` | body | `string` | yes | Updated incident description. |
| `urgency` | body | `string` | yes | Updated incident urgency. |
