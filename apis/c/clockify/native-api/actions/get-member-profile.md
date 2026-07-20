# Get Member Profile with Clockify

Retrieves a member profile from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/member-profile/:userId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Member Profile](https://docs.developer.clockify.me/#tag/User/operation/getMemberProfile)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
