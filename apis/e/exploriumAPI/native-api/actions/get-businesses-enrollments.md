# Get Businesses Enrollments with Explorium

Retrieves business event enrollments from Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses/events/enrollments`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Get Businesses Enrollments](https://developers.explorium.ai/reference/businesses/events/get_businesses_enrollments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_ids[]` | body | `array<string>` | yes | The Explorium business identifiers to enroll. |
| `enrollment_key` | body | `string` | yes | The client-defined enrollment key. |
| `event_types[]` | body | `array<string>` | yes | The business event types to enroll for. |
