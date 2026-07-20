# Update Group with Mode

Update a group in a Mode workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/[:groupToken]`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Update Group](https://mode.com/developer/api-reference/management/groups/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupToken` | path | `string` | yes | Mode group token. |
| `user_group` | body | `object` | yes | Group fields to update. |
