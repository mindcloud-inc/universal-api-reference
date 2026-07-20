# List Events with Zoho Backstage

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/portals/:portal_id/events`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [List Events](https://www.zoho.com/backstage/api/v3/get-all-events.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `status` | query | `string` | no | Filter events by lifecycle status. |
| `sort_by` | query | `string` | no | Sort events by a supported field. |
| `sort_order` | query | `string` | no | Sort direction for the event list. |
