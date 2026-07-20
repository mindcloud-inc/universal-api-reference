# Update Team Membership with SIGNL4

Updates a team membership in SIGNL4.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/teams/{teamId}/memberships/{userId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Update Team Membership](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Team the user you want to update belongs to at the moment. |
| `userId` | path | `string` | yes | User ID of user you want to update. |
| `requesterUserId` | query | `string` | no | User ID of user which you want to change role with. This must be provided when using an api key. This user must have role administrator (for setting administrator role) or team administrator (for setting rights. |
| `setUserOnDuty` | query | `boolean` | no | Sets new duty status for user if user is moved to a different team. User is on duty be default. |
| `teamId` | body | `string` | no | — |
| `roleId` | body | `string` | no | — |
| `isValid` | body | `boolean` | no | — |
