# Update Prospects Enrollments with Explorium

Updates prospect event enrollments in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/events/enrollments`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Update Prospects Enrollments](https://developers.explorium.ai/reference/prospects/events/update_prospects_enrollments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enrollment_key` | body | `string` | yes | The client-defined enrollment key. |
| `event_types[]` | body | `array<string>` | yes | The prospect event types to enroll for. |
| `prospect_ids[]` | body | `array<string>` | yes | The Explorium prospect identifiers to enroll. |
