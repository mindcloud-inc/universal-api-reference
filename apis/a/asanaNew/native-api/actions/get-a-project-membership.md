# Get a project membership with Asana

Retrieves a project membership from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `project_memberships/:project_membership_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a project membership](https://developers.asana.com/reference/getprojectmembership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `project_membership_gid` | path | `string` | yes | Path parameter: project_membership_gid |
