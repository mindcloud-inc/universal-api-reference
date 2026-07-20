# Create Incident with Pinghome

Creates a new incident in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/incident-cmd/v1/team/:id/incident`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Incident](https://docs.pinghome.io/incident-management/incident-tracking/create-incident/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Team ID for the incident. |
| `name` | body | `string` | yes | Incident name. |
| `description` | body | `string` | yes | Incident description. |
| `urgency` | body | `string` | yes | Incident urgency level. |
| `assignees[]` | body | `array<object>` | no | Optional assignee definitions. |
