# List Agendas with Zoho Backstage

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/portals/:portal_id/events/:event_id/agendas`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [List Agendas](https://www.zoho.com/backstage/api/v3/get-all-agendas.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
