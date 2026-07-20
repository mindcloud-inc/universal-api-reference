# List Attendees with Zoho Backstage

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/portals/:portal_id/events/:event_id/attendees`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [List Attendees](https://www.zoho.com/backstage/api/v3/get-all-attendees.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
| `ticket_id` | query | `string` | no | Filter attendees by ticket ID. |
