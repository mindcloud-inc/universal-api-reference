# Get User Balance with Clockify

Retrieves a user's time off balance from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/time-off/balance/user/:userId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get User Balance](https://docs.developer.clockify.me/#tag/Balance/operation/getBalancesForUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
