# Add Prospects Enrollments with Explorium

Adds prospect event enrollments in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/events/enrollments`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Add Prospects Enrollments](https://developers.explorium.ai/reference/prospects/events/add_prospects_enrollments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enrollment_key` | body | `string` | yes | The client-defined enrollment key. |
| `event_types[]` | body | `array<string>` | yes | The prospect event types to enroll for. |
| `prospect_ids[]` | body | `array<string>` | yes | The Explorium prospect identifiers to enroll. |
