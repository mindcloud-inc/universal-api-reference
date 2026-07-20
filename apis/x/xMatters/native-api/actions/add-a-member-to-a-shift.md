# Add a member to a shift with xMatters

Adds a member to a shift in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `groups/{groupId}/shifts/{shiftId}/members`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Add a member to a shift](https://help.xmatters.com/xmapi/index.html#add-a-member-to-a-shift)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `delay` | body | `number` | no |
| `escalationType` | body | `string` | no |
| `groupId` | path | `string` | no |
| `inRotation` | body | `boolean` | no |
| `onDuty` | body | `boolean` | no |
| `position` | body | `number` | no |
| `recipient` | body | `string` | no |
| `shiftId` | path | `string` | no |
