# Get Group Membership with Mode

Get details for a specific membership in a Mode group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/[:groupToken]/memberships/[:membershipToken]`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Get Group Membership](https://mode.com/developer/api-reference/management/group-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupToken` | path | `string` | yes | Mode group token. |
| `membershipToken` | path | `string` | yes | Mode group membership token. |
