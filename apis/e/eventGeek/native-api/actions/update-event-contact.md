# Update Event Contact with EventGeek

Updates an event contact in EventGeek.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/events/:event_id/contacts/:contact_id`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [Update Event Contact](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Circa contact identifier. |
| `event_id` | path | `string` | yes | Circa event identifier. |
