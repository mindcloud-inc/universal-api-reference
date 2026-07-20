# Get Event Person with Livestorm

Retrieves an event person from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `events/:eventId/people/:id`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Get Event Person](https://developers.livestorm.co/reference/get_events-event-id-people-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Event ID |
| `id` | path | `string` | yes | People ID |
