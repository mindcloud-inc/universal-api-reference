# Add User To Team with SIGNL4

Creates a team membership in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/teams/{teamId}/memberships/{userId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Add User To Team](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Id of team the user should be invited to. |
| `userId` | path | `string` | yes | Id of user you want to add to a team. |
| `roleId` | body | `string` | no | — |
| `setUserOnDuty` | body | `boolean` | no | — |
