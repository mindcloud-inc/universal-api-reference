# List Organization Users with Dev.to

Lists users in a Dev.to organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:username/users`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [List Organization Users](https://developers.forem.com/api/v1#tag/organizations/operation/getOrgUsers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Organization username. |
