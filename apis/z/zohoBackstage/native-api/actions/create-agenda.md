# Create Agenda with Zoho Backstage

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/portals/:portal_id/events/:event_id/agendas`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [Create Agenda](https://www.zoho.com/backstage/api/v3/create-an-agenda.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
| `index` | body | `number` | yes | — |
