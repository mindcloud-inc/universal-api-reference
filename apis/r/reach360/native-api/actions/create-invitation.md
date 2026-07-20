# Create Invitation with Reach360

Creates a new invitation in Reach360.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Create Invitation](https://www.articulatesupport.com/article/Reach-360-Invitations-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to invite. |
| `role` | body | `string` | yes | The role to assign to the invited user. |
| `groups` | body | `list<string>` | no | Groups to assign to the invited user. |
