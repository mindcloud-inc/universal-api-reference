# Update team membership status with Appwrite

Updates the team membership status in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/{teamId}/memberships/{membershipId}/status`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update team membership status](https://appwrite.io/docs/references/cloud/server-rest/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Team ID. |
| `membershipId` | path | `string` | yes | Membership ID. |
| `userId` | body | `string` | yes | User ID. |
| `secret` | body | `string` | yes | Secret key. |
