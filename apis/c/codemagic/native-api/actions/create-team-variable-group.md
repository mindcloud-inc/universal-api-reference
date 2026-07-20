# Create Team Variable Group with Codemagic

Creates a new variable group for a Codemagic team.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/teams/:team_id/variable-groups`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Create Team Variable Group](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3TeamsTeamIdVariableGroupsCreateVariableGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
| `name` | body | `string` | yes | Variable group name. Codemagic disallows periods and dollar signs. |
| `advanced_security` | body | `object` | yes | Advanced security object with enabled and selected_apps fields. |
