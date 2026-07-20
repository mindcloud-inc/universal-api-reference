# Delete Group with Mode

Delete a group from a Mode workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/[:groupToken]`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Delete Group](https://mode.com/developer/api-reference/management/groups/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupToken` | path | `string` | yes | Mode group token. |
