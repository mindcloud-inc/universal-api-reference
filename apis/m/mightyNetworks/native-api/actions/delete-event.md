# Delete Event with Mighty Networks

Deletes an existing event from Mighty Networks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/networks/:network_id/events/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Delete Event](https://docs.mightynetworks.com/api-reference/events/deletes-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID. |
| `id` | path | `number` | yes | The ID of the event to delete. |
