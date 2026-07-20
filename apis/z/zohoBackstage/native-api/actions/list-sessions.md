# List Sessions with Zoho Backstage

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/portals/:portal_id/events/:event_id/sessions`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [List Sessions](https://www.zoho.com/backstage/api/v3/get-all-sessions.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
| `day` | query | `number` | no | Return only sessions for a specific event day. |
