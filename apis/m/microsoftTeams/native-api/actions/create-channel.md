# Create Channel with Microsoft Teams

Creates a new channel in Microsoft Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/teams/:teamId/channels`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Channel](https://learn.microsoft.com/en-us/graph/api/channel-post?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Microsoft Graph team ID. |
| `displayName` | body | `string` | yes | Channel display name. |
| `description` | body | `string` | no | Optional channel description. |
| `membershipType` | body | `string` | no | Channel membership type. Use standard, private, or shared. |
