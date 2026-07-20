# Create Event with Mighty Networks

Creates a new event in Mighty Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/networks/:network_id/events`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Create Event](https://docs.mightynetworks.com/api-reference/events/creates-a-new-event-in-the-network)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID. |
| `space_id` | body | `number` | yes | The ID of the space that will host the event. |
| `title` | body | `string` | yes | The event title. |
| `starts_at` | body | `string` | yes | The event start time in ISO-8601 format. |
| `ends_at` | body | `string` | yes | The event end time in ISO-8601 format. |
| `event_type` | body | `string` | yes | The event type, such as online_meeting or local_meetup. |
| `description` | body | `string` | no | Optional event description. |
| `link` | body | `string` | no | Optional event link for online events. |
