# Remove Team Membership with SIGNL4

Deletes a team membership from SIGNL4.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/teams/{teamId}/memberships/{userId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Remove Team Membership](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | ID of the team the user should be deleted from |
| `userId` | path | `string` | yes | ID of the user that should be deleted |
| `requesterUserId` | query | `string` | no | User ID of user which will remove the other user. |
