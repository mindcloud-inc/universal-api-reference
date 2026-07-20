# Create Event with Zoho Backstage

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/portals/:portal_id/events`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [Create Event](https://www.zoho.com/backstage/api/v3/create-an-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `name` | body | `string` | yes | The event name. |
| `timezone` | body | `string` | yes | The event timezone. |
| `start_time` | body | `string` | yes | The event start time in UTC ISO 8601 format. |
| `end_time` | body | `string` | yes | The event end time in UTC ISO 8601 format. |
| `language` | body | `string` | no | The event language code. |
| `event_type` | body | `number` | no | The numeric event type: 2 venue, 3 online, 4 hybrid. |
| `summary` | body | `string` | no | A short summary of the event. |
| `description` | body | `string` | no | The event description. |
| `category` | body | `string` | no | The event category. |
