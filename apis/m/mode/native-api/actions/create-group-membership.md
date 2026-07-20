# Create Group Membership with Mode

Add a member to a group in a Mode workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/[:groupToken]/memberships`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Create Group Membership](https://mode.com/developer/api-reference/management/group-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupToken` | path | `string` | yes | Mode group token. |
| `membership` | body | `object` | yes | Membership fields to create. |
