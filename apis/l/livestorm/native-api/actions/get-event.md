# Get Event with Livestorm

Retrieves an event from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `events/:id`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Get Event](https://developers.livestorm.co/reference/get_events-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `include` | query | `string` | no | Include Related Data Send multiple values as a string separated by `,`. |
