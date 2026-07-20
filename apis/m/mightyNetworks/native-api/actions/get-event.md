# Get Event with Mighty Networks

Retrieves an event from Mighty Networks.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/events/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Get Event](https://docs.mightynetworks.com/api-reference/events/returns-details-of-a-specific-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `id` | path | `number` | yes | The ID of the event to retrieve. |
