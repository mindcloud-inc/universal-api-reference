# Get a workspace membership with Asana

Retrieves a workspace membership from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `workspace_memberships/:workspace_membership_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a workspace membership](https://developers.asana.com/reference/getworkspacemembership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `workspace_membership_gid` | path | `string` | yes | Path parameter: workspace_membership_gid |
