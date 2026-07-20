# Update Network Member with Mighty Networks

Updates a member's role in Mighty Networks.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/networks/:network_id/members/:id/`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [Update Network Member](https://docs.mightynetworks.com/api-reference/members/update-a-members-role-in-the-network)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
| `id` | path | `number` | yes | ID of the member. |
| `role` | body | `list<string>` | no | New role for the member. Accepted values: `contributor`, `host`, `moderator`. |
| `email` | body | `string` | no | New email address for the member. |
| `first_name` | body | `string` | no | New first name for the member. |
| `last_name` | body | `string` | no | New last name for the member. |
