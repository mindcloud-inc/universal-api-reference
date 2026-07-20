# Update Space with Mighty Networks

Updates an existing space in Mighty Networks.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/networks/:network_id/spaces/:id`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Update Space](https://docs.mightynetworks.com/api-reference/spaces/update-a-space-by-its-id-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | Network ID. |
| `id` | path | `number` | yes | Space ID. |
| `name` | body | `string` | no | Updated space name. |
| `collection_id` | body | `number` | no | Collection ID for the space. |
