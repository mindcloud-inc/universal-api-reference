# Create Organization Team with Cloudsmith

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org/teams/`
- **Base URL:** `https://api.cloudsmith.io`
- **Official documentation:** [Create Organization Team](https://help.cloudsmith.io/reference/orgs_teams_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org` | path | `string` | yes | Organization slug. |
| `name` | body | `string` | yes | Team name. |
| `description` | body | `string` | no | Team description. |
| `visibility` | body | `string` | no | Team visibility. |
