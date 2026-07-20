# List Team Members with Codemagic

Retrieves members for a specific Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/teams/:team_id/members`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Team Members](https://codemagic.io/api/v3/schema#tag/Team%20Members/operation/ApiV3TeamsTeamIdMembersListTeamMembers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
