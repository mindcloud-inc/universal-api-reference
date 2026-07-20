# Add Space Member with Mighty Networks

Adds a member to a space in Mighty Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/networks/:network_id/spaces/:space_id/members`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Add Space Member](https://docs.mightynetworks.com/api-reference/members/add-a-user-as-a-member-to-the-space)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `space_id` | path | `number` | yes | ID of the space. |
| `user_id` | query | `number` | yes | ID of the user to add. |
