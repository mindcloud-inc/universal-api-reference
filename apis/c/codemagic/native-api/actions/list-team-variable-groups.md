# List Team Variable Groups with Codemagic

Retrieves variable groups for a specific Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/teams/:team_id/variable-groups`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Team Variable Groups](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3TeamsTeamIdVariableGroupsGetVariableGroups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
