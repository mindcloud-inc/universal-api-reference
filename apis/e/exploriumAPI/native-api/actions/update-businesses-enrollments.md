# Update Businesses Enrollments with Explorium

Updates business event enrollments in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/events/enrollments`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Update Businesses Enrollments](https://developers.explorium.ai/reference/businesses/events/update_businesses_enrollments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_ids[]` | body | `array<string>` | yes | The Explorium business identifiers to enroll. |
| `enrollment_key` | body | `string` | yes | The client-defined enrollment key. |
| `event_types[]` | body | `array<string>` | yes | The business event types to enroll for. |
