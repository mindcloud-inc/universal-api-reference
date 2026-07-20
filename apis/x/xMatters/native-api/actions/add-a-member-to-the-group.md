# Add a member to the group with xMatters

Adds a member to the group in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `groups/{groupId}/members`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Add a member to the group](https://help.xmatters.com/xmapi/index.html#add-a-member-to-the-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | path | `string` | no |
| `id` | body | `string` | no |
| `recipientType` | body | `string` | no |
