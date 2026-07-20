# Create Session with Zoho Backstage

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/portals/:portal_id/events/:event_id/sessions`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [Create Session](https://www.zoho.com/backstage/api/v3/create-a-session.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
| `title` | body | `string` | yes | — |
| `track` | body | `string` | yes | — |
| `session_type` | body | `string` | yes | — |
| `start_time` | body | `string` | yes | — |
| `duration` | body | `number` | no | — |
| `venue` | body | `string` | no | — |
| `featured` | body | `boolean` | no | — |
| `venue_to_be_announced` | body | `boolean` | no | — |
| `hidden` | body | `boolean` | no | — |
| `speakers[]` | body | `array<string>` | no | — |
| `time_to_be_announced` | body | `boolean` | no | — |
