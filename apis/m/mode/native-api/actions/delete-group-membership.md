# Delete Group Membership with Mode

Remove a member from a group in a Mode workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/[:groupToken]/memberships/[:membershipToken]`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Delete Group Membership](https://mode.com/developer/api-reference/management/group-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupToken` | path | `string` | yes | Mode group token. |
| `membershipToken` | path | `string` | yes | Mode group membership token. |
