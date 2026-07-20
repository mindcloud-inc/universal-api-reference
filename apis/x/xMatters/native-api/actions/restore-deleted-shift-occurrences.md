# Restore deleted shift occurrences with xMatters

Restores deleted shift occurrences in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `groups/{groupId}/shifts/{shiftId}/occurrences`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Restore deleted shift occurrences](https://help.xmatters.com/xmapi/index.html#restore-deleted-shift-occurrences)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endDate` | body | `string` | no |
| `groupId` | path | `string` | no |
| `shiftId` | path | `string` | no |
| `startDate` | body | `string` | no |
