# Delete Space with Mighty Networks

Deletes an existing space from Mighty Networks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/networks/:network_id/spaces/:id`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Delete Space](https://docs.mightynetworks.com/api-reference/spaces/delete-a-space-by-its-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID. |
| `id` | path | `number` | yes | The ID of the space to delete. |
