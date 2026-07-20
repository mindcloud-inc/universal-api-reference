# Remove Space Member with Mighty Networks

Removes a member from a space in Mighty Networks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/networks/:network_id/spaces/:space_id/members/:user_id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Remove Space Member](https://docs.mightynetworks.com/api-reference/members/remove-a-member-from-the-space)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `space_id` | path | `number` | yes | ID of the space. |
| `user_id` | path | `number` | yes | ID of the user to remove. |
