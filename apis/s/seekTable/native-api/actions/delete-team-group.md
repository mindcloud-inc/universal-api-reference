# Delete Team Group with SeekTable

Deletes an existing team group from SeekTable.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/account/:id/team/group/:group_id`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Delete Team Group](https://www.seektable.com/help/self-hosted-admin-accounts-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the user account that owns the team. |
| `group_id` | path | `string` | yes | ID of the team group. |
