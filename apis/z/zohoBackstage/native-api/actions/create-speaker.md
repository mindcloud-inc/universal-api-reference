# Create Speaker with Zoho Backstage

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/portals/:portal_id/events/:event_id/speakers`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [Create Speaker](https://www.zoho.com/backstage/api/v3/create-a-speaker.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
| `email` | body | `string` | yes | — |
| `name` | body | `string` | yes | — |
| `last_name` | body | `string` | no | — |
| `country` | body | `string` | no | — |
| `featured` | body | `boolean` | no | — |
| `company` | body | `string` | no | — |
| `designation` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `telephone` | body | `string` | no | — |
| `alternate_telephone` | body | `string` | no | — |
| `skills` | body | `string` | no | — |
