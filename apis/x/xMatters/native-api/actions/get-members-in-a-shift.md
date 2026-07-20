# Get members in a shift with xMatters

Retrieves members in a shift from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `groups/{groupId}/shifts/{shiftId}/members`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get members in a shift](https://help.xmatters.com/xmapi/index.html#get-members-in-a-shift)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | path | `string` | no |
| `shiftId` | path | `string` | no |
