# Update Organization Team with Cloudsmith

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orgs/:org/teams/:team/`
- **Base URL:** `https://api.cloudsmith.io`
- **Official documentation:** [Update Organization Team](https://help.cloudsmith.io/reference/orgs_teams_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org` | path | `string` | yes | Organization slug. |
| `team` | path | `string` | yes | Team slug. |
| `name` | body | `string` | no | Updated team name. |
| `description` | body | `string` | no | Updated team description. |
| `visibility` | body | `string` | no | Updated team visibility. |
